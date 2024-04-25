**Kubernetes Aliases**

This section provides a list of helpful aliases designed to streamline your workflow when working with Kubernetes using `kubectl`. These aliases offer quicker access to frequently used commands and enhance efficiency.

**How to Use Aliases**

1. **Add to Shell Configuration:** Copy and paste the alias definitions below into your shell configuration file (e.g., `.bashrc` for Bash).
2. **Save and Reload:** Save your changes to the configuration file and then reload your shell session for the aliases to take effect (usually by sourcing the file or restarting the terminal).

**Available Aliases for kubectl commands:**

- `k=kubectl`: This is a simple alias that assigns the `kubectl` command to the shorter `k`. This saves you from typing the full command repeatedly.
- `kn='kubectl config set-context --current --namespace'`: Sets the current namespace for `kubectl` commands. You provide the namespace after the `kn` alias.
- `gn='cat .kube/config | grep namespace'`: Displays the currently active namespace by searching the `.kube/config` file for the `namespace` property.
- `kg='k get'`: An alias for `kubectl get`, used to retrieve information about various Kubernetes resources (deployments, pods, etc.).
- `kgd='k get deploy -o wide'`: Retrieves details about deployments in wide format for better readability.
- `kgp='k get pods -o wide'`: Gets information about pods in wide format.
- `kgpw='k get pods -o wide --watch'`: Similar to `kgp` but continuously shows updates to pod information.
- `kgpa='k get pods -o wide -A'`: Retrieves pod details from all namespaces (use with caution).
- `kgn='k get nodes -o wide'`: Shows details about Kubernetes worker nodes in wide format.
- `kgs='k get svc -o wide'`: Retrieves information about services in wide format.
- `kge='k get events --sort-by='.metadata.creationTimestamp' | tail -8'`: Shows the most recent 8 events sorted by creation time.
- `ked='k edit deploy'`: Opens the current deployment definition in an editor for modification.
- `kep='k edit pods'`: Similar to `ked`, but for editing pod definitions.
- `ken='k edit nodes'`: Allows editing of node configurations (use with caution).
- `kes='k edit svc'`: Opens the current service definition for editing.
- `kc='k create'`: A shortcut for `kubectl create`, used to create new Kubernetes resources.
- `kd='k describe'`: Shows detailed information about a specific resource using `kubectl describe`.
  - Variations like `kdd`, `kdp`, `kdn`, and `kds` provide more specific descriptions for deployments, pods, nodes, and services, respectively.

**Environment variables:**

- `export nks='-n kube-system'`: Sets a default namespace (`kube-system`) for some commands. You can override this with `-n <namespace>` while using commands like `kg`.
- `export do=' --dry-run=client -o yaml'`: Used for a "dry run" of commands, showing what would happen without actually making changes. Outputs the YAML representation of the intended change.
- `export now=' --force --grace-period=0'`: Forces deletion of resources and sets the grace period to 0 (immediate deletion). Use with caution as it bypasses safety measures.
- `export rb='rolebinding'`: An alias for `rolebinding` resource type.
- `export crb='clusterrolebinding'`: An alias for `clusterrolebinding` resource type.

**Additional notes:**

- These aliases are designed to make working with `kubectl` more efficient by providing shorter commands and defaults.
- Be cautious with commands like `kdel` and `kdelp` as they can lead to unintended resource deletion.
- Consider customizing these aliases to fit your specific workflow and preferences.
- Refer to the official `kubectl` documentation for detailed information on each command and its options: [https://kubernetes.io/docs/home/](https://kubernetes.io/docs/home/)
