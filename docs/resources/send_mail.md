---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "smtp_send_mail Resource - smtp"
subcategory: ""
description: |-
  Send a email with smtp. Note: At this moment authentication-less access to smtp and TLS validation is not support.
---

# smtp_send_mail (Resource)

Send a email with smtp. Note: At this moment authentication-less access to smtp and TLS validation is not support.

## Example Usage

```terraform
resource "smtp_send_mail" "this" {
  to      = "to@example.com"
  from    = "from@example.com"
  subject = "First Terraform plugin"
  body    = "My first mail goes good."
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `body` (String) Body of the email.
- `subject` (String) Subject of the email.
- `to` (List of String) To email addresses.

### Optional

- `bcc` (List of String) BCC email addresses.
- `cc` (List of String) CC email addresses.
- `from` (String) From email address. If not provided, the username used in the smtp auth will be used.
- `render_html` (Boolean) Boolean flag is identify whether the body is html or plain text. Set this to `true` if body is a HTML content.

### Read-Only

- `id` (String) Autogenerated id for the resource.


