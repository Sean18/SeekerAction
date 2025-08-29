# Setup Seeker Agent Action

This action downloads and sets up the BlackDuck Seeker security testing agent for Java applications.

## Inputs

| Input | Description | Required | Default |
|-------|-------------|----------|---------|
| `base-url` | Base URL for the Seeker server | Yes | `https://seeker.field-test.blackduck.com` |
| `project-key` | Project key for Seeker | Yes | - |
| `agent-name` | Name for the Seeker agent | No | `""` |
| `access-token` | Access token for Seeker API | Yes | - |
| `os-family` | Operating system family | No | `LINUX` |
| `web-server` | Web server type | No | `OTHER` |
| `flavor` | Agent flavor | No | `DEFAULT` |
| `output-path` | Path where to copy the seeker-agent.jar | No | `test/seeker-agent.jar` |

## Outputs

| Output | Description |
|--------|-------------|
| `agent-path` | Path to the downloaded seeker agent jar |

## Example Usage

```yaml
- name: Setup Seeker Agent
  uses: your-username/setup-seeker-agent-action@v1
  with:
    base-url: 'https://seeker.field-test.blackduck.com'
    project-key: 'hippotech_github'
    agent-name: 'my-test-agent'
    access-token: ${{ secrets.SEEKER_ACCESS_TOKEN }}
    output-path: 'test/seeker-agent.jar'
```

## License

MIT