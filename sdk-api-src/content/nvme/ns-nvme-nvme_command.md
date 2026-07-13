---
UID: NS:nvme.NVME_COMMAND
tech.root: fs
title: NVME_COMMAND
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains the parameters for all commands in the Admin Command and NVM Command sets.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: NVME_COMMAND, *PNVME_COMMAND
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_COMMAND
 - NVME_COMMAND
f1_keywords:
 - PNVME_COMMAND
 - nvme/PNVME_COMMAND
 - NVME_COMMAND
 - nvme/NVME_COMMAND
dev_langs:
 - c++
---

# NVME_COMMAND structure


## -description

Contains the parameters for all commands in the Admin Command and NVM Command sets.

## -struct-fields

### -field CDW0

A [NVME_COMMAND_DWORD0](ns-nvme-nvme_command_dword0.md) structure containing parameters that are common for all Admin and NVM commands.

### -field NSID

The namespace ID that this command applies to.

If the namespace ID is not used for the command, then this field should cleared to `0h`. If a command is applied to all namespaces accessible by this controller, then this field should be set to `FFFFFFFFh`.

Unless otherwise noted, specifying an inactive namespace ID in a command that uses the namespace ID will cause the controller to abort the command with the status [NVME_STATUS_INVALID_FIELD_IN_COMMAND](ne-nvme-nvme_status_generic_command_codes.md#-field-nvme-status-invalid-field-in-command). Specifying an invalid namespace ID in a command that uses the namespace ID will cause the controller to abort the command with the status [NVME_STATUS_INVALID_NAMESPACE_OR_FORMAT](ne-nvme-nvme_status_generic_command_codes.md#-field-nvme-status-invalid-namespace-or-format).

### -field Reserved0

### -field MPTR

The address of a contiguous physical buffer of metadata.

This field is only used if metadata is not interleaved with the logical block data, as specified in the **MS** field of the [NVME_CDW10_FORMAT_NVM](ns-nvme-nvme_cdw10_format_nvm.md) command structure. This field is Dword aligned.

### -field PRP1

A [NVME_PRP_ENTRY](ns-nvme-nvme_prp_entry.md) structure that contains the first PRP entry for the command or a PRP List pointer depending on the command.

### -field PRP2

This field is reserved if the data transfer does not cross a memory page boundary. Otherwise, it contains a [NVME_PRP_ENTRY](ns-nvme-nvme_prp_entry.md) structure that:

1. Specifies the Page Base Address of the second memory page if the data transfer crosses exactly one memory page boundary. For example, in one of the following situations:

   - The command data transfer length is equal in size to one memory page and the offset portion of the Page Base Address and Offset (**PBAO**) field of **PRP1** is non-zero.
   - The Offset portion of the **PBAO** field of **PRP1** is equal to zero and the command data transfer length is greater than one memory page and less than or equal to two memory pages in size.

2. Is a PRP List pointer if the data transfer crosses more than one memory page boundary. For example, in one of the following situations:

   - The command data transfer length is greater than or equal to two memory pages in size but the offset portion of the **PBAO** field of **PRP1** is non-zero.
   - The command data transfer length is equal in size to more than two memory pages and the Offset portion of the **PBAO** field of **PRP1** is equal to zero.

### -field u

A union of all the command structures.

### -field u.GENERAL

A structure containing data fields for General commands.

### -field u.GENERAL.CDW10

Command DWord 10 data fields for General commands.

### -field u.GENERAL.CDW11

Command DWord 11 data fields for General commands.

### -field u.GENERAL.CDW12

Command DWord 12 data fields for General commands.

### -field u.GENERAL.CDW13

Command DWord 13 data fields for General commands.

### -field u.GENERAL.CDW14

Command DWord 14 data fields for General commands.

### -field u.GENERAL.CDW15

Command DWord 15 data fields for General commands.

### -field u.IDENTIFY

A structure containing parameters for the Identify Command. An Admin command that returns a data buffer describing information about the NVM subsystem, the controller or the namespace(s).

The Identify command uses the PRP Entry 1 (**PRP1**), PRP Entry 2 (**PRP2**), Command Dword 10 (**CDW10**), and Command Dword 11 (**CDW11**) fields. All other command specific fields are reserved.

### -field u.IDENTIFY.CDW10

A [NVME_CDW10_IDENTIFY](ns-nvme-nvme_cdw10_identify.md) structure containing Command DWord 10 parameters for the Identify Command.

### -field u.IDENTIFY.CDW11

A [NVME_CDW11_IDENTIFY](ns-nvme-nvme_cdw11_identify.md) structure containing Command DWord 11 parameters for the Identify Command.

### -field u.IDENTIFY.CDW12

Command DWord 12 data fields for the Identify Command.

### -field u.IDENTIFY.CDW13

Command DWord 13 data fields for the Identify Command.

### -field u.IDENTIFY.CDW14

Command DWord 14 data fields for the Identify Command.

### -field u.IDENTIFY.CDW15

Command DWord 15 data fields for the Identify Command.

### -field u.ABORT

A structure containing parameters for the Abort Command. An Admin command that is used to abort a specific command previously submitted to the Admin Submission Queue or an I/O Submission Queue.

The Abort command uses Command Dword 10 (**CDW10**) fields. All other command specific fields are reserved.

### -field u.ABORT.CDW10

A [NVME_CDW10_ABORT](ns-nvme-nvme_cdw10_abort.md) structure containing Command DWord 10 parameters for the Abort Command.

### -field u.ABORT.CDW11

Command DWord 11 data fields for the Abort Command.

### -field u.ABORT.CDW12

Command DWord 12 data fields for the Abort Command.

### -field u.ABORT.CDW13

Command DWord 13 data fields for the Abort Command.

### -field u.ABORT.CDW14

Command DWord 14 data fields for the Abort Command.

### -field u.ABORT.CDW15

Command DWord 15 data fields for the Abort Command.

### -field u.GETFEATURES

A structure containing parameters for the Get Features Command. An Admin command that retrieves the attributes of a specified feature.

The Get Features command uses the PRP Entry 1 (**PRP1**), PRP Entry 2 (**PRP2**), Command Dword 10 (**CDW10**), and Command Dword 11 (**CDW11**) fields. All other command specific fields are reserved.

### -field u.GETFEATURES.CDW10

A [NVME_CDW10_GET_FEATURES](ns-nvme-nvme_cdw10_get_features.md) structure containing Command DWord 10 parameters for the Get Features command.

### -field u.GETFEATURES.CDW11

A [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure containing Command DWord 11 parameters for the Get Features command.

### -field u.GETFEATURES.CDW12

Command DWord 12 data fields for the Get Features command.

### -field u.GETFEATURES.CDW13

Command DWord 13 data fields for the Get Features command.

### -field u.GETFEATURES.CDW14

Command DWord 14 data fields for the Get Features command.

### -field u.GETFEATURES.CDW15

Command DWord 15 data fields for the Get Features command.

### -field u.SETFEATURES

A structure containing parameters for the Set Features Command. An Admin command that sets the attributes of a specified feature.

The Set Features command uses the PRP Entry 1 (**PRP1**), PRP Entry 2 (**PRP2**), Command Dword 10 (**CDW10**), Command Dword 11 (**CDW11**), Command Dword 12 (**CDW12**), Command Dword 13 (**CDW13**), Command Dword 14 (**CDW14**), and Command Dword 15 (**CDW15**) fields. All other command specific fields are reserved.

### -field u.SETFEATURES.CDW10

A [NVME_CDW10_SET_FEATURES](ns-nvme-nvme_cdw10_set_features.md) structure containing Command DWord 10 parameters for the Set Features command.

### -field u.SETFEATURES.CDW11

A [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure containing Command DWord 11 parameters for the Set Features command.

### -field u.SETFEATURES.CDW12

A [NVME_CDW12_FEATURES](ns-nvme-nvme_cdw12_features.md) structure containing Command DWord 12 parameters for the Set Features command.

### -field u.SETFEATURES.CDW13

A [NVME_CDW13_FEATURES](ns-nvme-nvme_cdw13_features.md) structure containing Command DWord 13 parameters for the Set Features command.

### -field u.SETFEATURES.CDW14

A [NVME_CDW14_FEATURES](ns-nvme-nvme_cdw14_features.md) structure containing Command DWord 14 parameters for the Set Features command.

### -field u.SETFEATURES.CDW15

A [NVME_CDW15_FEATURES](ns-nvme-nvme_cdw15_features.md) structure containing Command DWord 15 parameters for the Set Features command.

### -field u.GETLOGPAGE

A structure containing parameters for the Get Log Page Command. An Admin command that returns a data buffer containing the requested log page.

The Get Log Page command uses the PRP Entry 1 (**PRP1**), PRP Entry 2 (**PRP2**), Command Dword 10 (**CDW10** and **CDW10_V13**), Command Dword 11 (**CDW11**), Command Dword 12 (**CDW12**), and Command Dword 13 (**CDW13**) fields. All other command specific fields are reserved.

### -field u.GETLOGPAGE.CDW10

A [NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md) structure containing Command DWord 10 parameters for the Get Log Page command that conform to NVMe Specifications prior to version 1.3.

### -field u.GETLOGPAGE.CDW10_V13

A [NVME_CDW10_GET_LOG_PAGE_V13](ns-nvme-nvme_cdw10_get_log_page_v13.md) structure containing Command DWord 10 parameters for the Get Log Page command that conform to NVMe Specification version 1.3 or later.

### -field u.GETLOGPAGE.CDW11

A [NVME_CDW11_GET_LOG_PAGE](ns-nvme-nvme_cdw11_get_log_page.md) structure containing Command DWord 11 parameters for the Get Log Page command.

### -field u.GETLOGPAGE.CDW12

A [NVME_CDW12_GET_LOG_PAGE](ns-nvme-nvme_cdw12_get_log_page.md) structure containing Command DWord 12 parameters for the Get Log Page command.

### -field u.GETLOGPAGE.CDW13

A [NVME_CDW13_GET_LOG_PAGE](ns-nvme-nvme_cdw13_get_log_page.md) structure containing Command DWord 13 parameters for the Get Log Page command.

### -field u.GETLOGPAGE.CDW14

Command DWord 14 data fields for the Get Log Page command.

### -field u.GETLOGPAGE.CDW15

Command DWord 15 data fields for the Get Log Page command.

### -field u.CREATEIOCQ

A structure containing parameters for the Create IO Completion Queue Command. An Admin command that is used to create all I/O Completion Queues with the exception of the Admin Completion Queue.

The Create IO Completion Queue command uses the PRP Entry 1 (**PRP1**), Command Dword 10 (**CDW10**), and Command Dword 11 (**CDW11**) fields. All other command specific fields are reserved.

### -field u.CREATEIOCQ.CDW10

A [NVME_CDW10_CREATE_IO_QUEUE](ns-nvme-nvme_cdw10_create_io_queue.md) structure containing Command DWord 10 parameters for the Create IO Completion Queue command.

### -field u.CREATEIOCQ.CDW11

A [NVME_CDW11_CREATE_IO_CQ](ns-nvme-nvme_cdw11_create_io_cq.md) structure containing Command DWord 11 parameters for the Create IO Completion Queue command.

### -field u.CREATEIOCQ.CDW12

Command DWord 12 data fields for the Create IO Completion Queue command.

### -field u.CREATEIOCQ.CDW13

Command DWord 13 data fields for the Create IO Completion Queue command.

### -field u.CREATEIOCQ.CDW14

Command DWord 14 data fields for the Create IO Completion Queue command.

### -field u.CREATEIOCQ.CDW15

Command DWord 15 data fields for the Create IO Completion Queue command.

### -field u.CREATEIOSQ

A structure containing parameters for the Create IO Submission Queue Command. An Admin command that is used to create I/O Submission Queues.

The Create IO Submission Queue command uses the PRP Entry 1 (**PRP1**), Command Dword 10 (**CDW10**), and Command Dword 11 (**CDW11**) fields. All other command specific fields are reserved.

### -field u.CREATEIOSQ.CDW10

A [NVME_CDW10_CREATE_IO_QUEUE](ns-nvme-nvme_cdw10_create_io_queue.md) structure containing Command DWord 10 parameters for the Create IO Submission Queue command.

### -field u.CREATEIOSQ.CDW11

A [NVME_CDW11_CREATE_IO_SQ](ns-nvme-nvme_cdw11_create_io_sq.md) structure containing Command DWord 11 parameters for the Create IO Submission Queue command.

### -field u.CREATEIOSQ.CDW12

Command DWord 12 data fields for the Create IO Submission Queue command.

### -field u.CREATEIOSQ.CDW13

Command DWord 13 data fields for the Create IO Submission Queue command.

### -field u.CREATEIOSQ.CDW14

Command DWord 14 data fields for the Create IO Submission Queue command.

### -field u.CREATEIOSQ.CDW15

Command DWord 15 data fields for the Create IO Submission Queue command.

### -field u.DATASETMANAGEMENT

A structure containing parameters for the Dataset Management Command. An NVM command that is used by the host to indicate attributes for ranges of logical blocks.

The Dataset Management command uses Command Dword 10 (**CDW10**) and Command Dword 11 (**CDW11**) fields. If the command uses PRPs for the data transfer, then the PRP Entry 1 (**PRP1**) and PRP Entry 2 (**PRP2**) fields are used. All other command specific fields are reserved.

### -field u.DATASETMANAGEMENT.CDW10

A [NVME_CDW10_DATASET_MANAGEMENT](ns-nvme-nvme_cdw10_dataset_management.md) structure containing Command DWord 10 parameters for the Dataset Management command.

### -field u.DATASETMANAGEMENT.CDW11

A [NVME_CDW11_DATASET_MANAGEMENT](ns-nvme-nvme_cdw11_dataset_management.md) structure containing Command DWord 11 parameters for the Dataset Management command.

### -field u.DATASETMANAGEMENT.CDW12

Command DWord 12 data fields for the Dataset Management command.

### -field u.DATASETMANAGEMENT.CDW13

Command DWord 13 data fields for the Dataset Management command.

### -field u.DATASETMANAGEMENT.CDW14

Command DWord 14 data fields for the Dataset Management command.

### -field u.DATASETMANAGEMENT.CDW15

Command DWord 15 data fields for the Dataset Management command.

### -field u.SECURITYSEND

A structure containing parameters for the Security Send Command. An Admin command that is used to transfer security protocol data to the controller.

The Security Send command uses PRP Entry 1 (**PRP1**), PRP Entry 2 (**PRP2**), Command Dword 10 (**CDW10**), and Command Dword 11 (**CDW11**) fields. All other command specific fields are reserved.

### -field u.SECURITYSEND.CDW10

A [NVME_CDW10_SECURITY_SEND_RECEIVE](ns-nvme-nvme_cdw10_security_send_receive.md) structure containing Command DWord 10 parameters for the Security Send command.

### -field u.SECURITYSEND.CDW11

A [NVME_CDW11_SECURITY_SEND](ns-nvme-nvme_cdw11_security_send.md) structure containing Command DWord 11 parameters for the Security Send command.

### -field u.SECURITYSEND.CDW12

Command DWord 12 data fields for the Security Send command.

### -field u.SECURITYSEND.CDW13

Command DWord 13 data fields for the Security Send command.

### -field u.SECURITYSEND.CDW14

Command DWord 14 data fields for the Security Send command.

### -field u.SECURITYSEND.CDW15

Command DWord 15 data fields for the Security Send command.

### -field u.SECURITYRECEIVE

A structure containing parameters for the Security Receive Command. An Admin command that transfers the status and data result of one or more [Security Send](#-field-u.securitysend) commands that were previously submitted to the controller.

The Security Receive command uses PRP Entry 1 (**PRP1**), PRP Entry 2 (**PRP2**), Command Dword 10 (**CDW10**), and Command Dword 11 (**CDW11**) fields. All other command specific fields are reserved.

### -field u.SECURITYRECEIVE.CDW10

A [NVME_CDW10_SECURITY_SEND_RECEIVE](ns-nvme-nvme_cdw10_security_send_receive.md) structure containing Command DWord 10 parameters for the Security Receive command.

### -field u.SECURITYRECEIVE.CDW11

A [NVME_CDW11_SECURITY_RECEIVE](ns-nvme-nvme_cdw11_security_receive.md) structure containing Command DWord 11 parameters for the Security Receive command.

### -field u.SECURITYRECEIVE.CDW12

Command DWord 12 data fields for the Security Receive command.

### -field u.SECURITYRECEIVE.CDW13

Command DWord 13 data fields for the Security Receive command.

### -field u.SECURITYRECEIVE.CDW14

Command DWord 14 data fields for the Security Receive command.

### -field u.SECURITYRECEIVE.CDW15

Command DWord 15 data fields for the Security Receive command.

### -field u.FIRMWAREDOWNLOAD

A structure containing parameters for the Firmware Image Download Command. An Admin command that is used to copy a new firmware image (in whole or in part) to the controller.

The Firmware Image Download command uses the PRP Entry 1 (**PRP1**), PRP Entry 2 (**PRP2**), Command Dword 10 (**CDW10**), and Command Dword 11 (**CDW11**) fields. All other command specific fields are reserved.

### -field u.FIRMWAREDOWNLOAD.CDW10

A [NVME_CDW10_FIRMWARE_DOWNLOAD](ns-nvme-nvme_cdw10_firmware_download.md) structure containing Command DWord 10 parameters for the Firmware Image Download command.

### -field u.FIRMWAREDOWNLOAD.CDW11

A [NVME_CDW11_FIRMWARE_DOWNLOAD](ns-nvme-nvme_cdw11_firmware_download.md) structure containing Command DWord 11 parameters for the Firmware Image Download command.

### -field u.FIRMWAREDOWNLOAD.CDW12

Command DWord 12 data fields for the Firmware Image Download command.

### -field u.FIRMWAREDOWNLOAD.CDW13

Command DWord 13 data fields for the Firmware Image Download command.

### -field u.FIRMWAREDOWNLOAD.CDW14

Command DWord 14 data fields for the Firmware Image Download command.

### -field u.FIRMWAREDOWNLOAD.CDW15

Command DWord 15 data fields for the Firmware Image Download command.

### -field u.FIRMWAREACTIVATE

A structure containing parameters for the Firmware Commit Command. An Admin command that is used to verify that a valid firmware image has been downloaded and to commit that revision to a specific firmware slot.

> [!NOTE]
> The Firmware Commit command was called Firmware Activate in previous versions of NVM Express.

The Firmware Commit command uses the Command Dword 10 (**CDW10**) field. All other command specific fields are reserved.

### -field u.FIRMWAREACTIVATE.CDW10

A [NVME_CDW10_FIRMWARE_ACTIVATE](ns-nvme-nvme_cdw10_firmware_activate.md) structure containing Command DWord 10 parameters for the Firmware Commit  command.

### -field u.FIRMWAREACTIVATE.CDW11

Command DWord 11 data fields for the Firmware Commit command.

### -field u.FIRMWAREACTIVATE.CDW12

Command DWord 12 data fields for the Firmware Commit command.

### -field u.FIRMWAREACTIVATE.CDW13

Command DWord 13 data fields for the Firmware Commit command.

### -field u.FIRMWAREACTIVATE.CDW14

Command DWord 14 data fields for the Firmware Commit command.

### -field u.FIRMWAREACTIVATE.CDW15

Command DWord 15 data fields for the Firmware Commit command.

### -field u.FORMATNVM

A structure containing parameters for the Format NVM Command. An Admin command that is used to low level format the NVM media.

The Format NVM command uses the Command Dword 10 (**CDW10**) field. All other command specific fields are reserved.

### -field u.FORMATNVM.CDW10

A [NVME_CDW10_FORMAT_NVM](ns-nvme-nvme_cdw10_format_nvm.md) structure containing Command DWord 10 parameters for the Format NVM command.

### -field u.FORMATNVM.CDW11

Command DWord 11 data fields for the Format NVM command.

### -field u.FORMATNVM.CDW12

Command DWord 12 data fields for the Format NVM command.

### -field u.FORMATNVM.CDW13

Command DWord 13 data fields for the Format NVM command.

### -field u.FORMATNVM.CDW14

Command DWord 14 data fields for the Format NVM command.

### -field u.FORMATNVM.CDW15

Command DWord 15 data fields for the Format NVM command.

### -field u.DIRECTIVERECEIVE

A structure containing parameters for the Admin Command Directive Receive.

The Directive Receive command uses the Command Dword 10 (**CDW10**), Command Dword 11 (**CDW11**), and Command Dword 12 (**CDW12**) fields. All other command specific fields are reserved.

### -field u.DIRECTIVERECEIVE.CDW10

A [NVME_CDW10_DIRECTIVE_RECEIVE](ns-nvme-nvme_cdw10_directive_receive.md) structure containing Command DWord 10 parameters for the Directive Receive command.

### -field u.DIRECTIVERECEIVE.CDW11

A [NVME_CDW11_DIRECTIVE_RECEIVE](ns-nvme-nvme_cdw11_directive_receive.md) structure containing Command DWord 11 parameters for the Directive Receive command.

### -field u.DIRECTIVERECEIVE.CDW12

A [NVME_CDW12_DIRECTIVE_RECEIVE](ns-nvme-nvme_cdw12_directive_receive.md) structure containing Command DWord 12 parameters for the Directive Receive command.

### -field u.DIRECTIVERECEIVE.CDW13

Command DWord 13 data fields for the Directive Receive command.

### -field u.DIRECTIVERECEIVE.CDW14

Command DWord 14 data fields for the Directive Receive command.

### -field u.DIRECTIVERECEIVE.CDW15

Command DWord 15 data fields for the Directive Receive command.

### -field u.DIRECTIVESEND

A structure containing parameters for the Admin Command Directive Send.

The Directive Send command uses the Command Dword 10 (**CDW10**), Command Dword 11 (**CDW11**), and Command Dword 12 (**CDW12**) fields. All other command specific fields are reserved.

### -field u.DIRECTIVESEND.CDW10

A [NVME_CDW10_DIRECTIVE_SEND](ns-nvme-nvme_cdw10_directive_send.md) structure containing Command DWord 10 parameters for the Directive Send command.

### -field u.DIRECTIVESEND.CDW11

A [NVME_CDW11_DIRECTIVE_SEND](ns-nvme-nvme_cdw11_directive_send.md) structure containing Command DWord 11 parameters for the Directive Send command.

### -field u.DIRECTIVESEND.CDW12

A [NVME_CDW12_DIRECTIVE_SEND](ns-nvme-nvme_cdw12_directive_send.md) structure containing Command DWord 12 parameters for the Directive Send command.

### -field u.DIRECTIVESEND.CDW13

Command DWord 13 data fields for the Directive Send command.

### -field u.DIRECTIVESEND.CDW14

Command DWord 14 data fields for the Directive Send command.

### -field u.DIRECTIVESEND.CDW15

Command DWord 15 data fields for the Directive Send command.

### -field u.READWRITE

A structure containing parameters for the NVME Read and NVME Write commands that read or write data and metadata, if applicable, to and from the NVM controller for the specified Logical Block Addresses (LBA).

The NVME Read and NVME Write commands use the Command Dword 12 (**CDW12**), Command Dword 13 (**CDW13**), and Command Dword 14 (**CDW14**) fields.

### -field u.READWRITE.LBALOW

The low LBA.

### -field u.READWRITE.LBAHIGH

The high LBA.

### -field u.READWRITE.CDW12

A [NVME_CDW12_READ_WRITE](ns-nvme-nvme_cdw12_read_write.md) structure containing Command DWord 12 parameters for the NVME Read and NVME Write commands.

### -field u.READWRITE.CDW13

A [NVME_CDW13_READ_WRITE](ns-nvme-nvme_cdw13_read_write.md) structure containing Command DWord 13 parameters for the NVME Read and NVME Write commands.

### -field u.READWRITE.CDW14

Command DWord 14 data fields for the NVME Read and NVME Write commands.

### -field u.READWRITE.CDW15

A [NVME_CDW15_READ_WRITE](ns-nvme-nvme_cdw15_read_write.md) structure containing Command DWord 15 parameters for the NVME Read and NVME Write commands.

## -remarks

The Admin Command Set defines the commands that may be submitted to the Admin Submission Queue.

For all Admin commands, DWord 14 and DWord 15 are I/O Command Set specific.

## -see-also

