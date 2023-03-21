---
UID: NE:nvme.NVME_ADMIN_COMMANDS
tech.root: fs
title: NVME_ADMIN_COMMANDS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Defines values that specify a command in the Admin command set which. The Admin command set contains commands that may be submitted to the Admin Submission Queue.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_ADMIN_COMMANDS
f1_keywords:
 - NVME_ADMIN_COMMANDS
 - nvme/NVME_ADMIN_COMMANDS
dev_langs:
 - c++
---

# NVME_ADMIN_COMMANDS enumeration


## -description

Defines values that specify a command in the Admin command set which. The Admin command set contains commands that may be submitted to the Admin Submission Queue.

## -enum-fields

### -field NVME_ADMIN_COMMAND_DELETE_IO_SQ

The Delete I/O Submission Queue command.

### -field NVME_ADMIN_COMMAND_CREATE_IO_SQ

The Create I/O Submission Queue command.

### -field NVME_ADMIN_COMMAND_GET_LOG_PAGE

The Get Log Page command.

### -field NVME_ADMIN_COMMAND_DELETE_IO_CQ

The Delete I/O Completion Queue command.

### -field NVME_ADMIN_COMMAND_CREATE_IO_CQ

The Create I/O Completion Queue command.

### -field NVME_ADMIN_COMMAND_IDENTIFY

The Identify command.

### -field NVME_ADMIN_COMMAND_ABORT

The Abort command.

### -field NVME_ADMIN_COMMAND_SET_FEATURES

The Set Features command.

### -field NVME_ADMIN_COMMAND_GET_FEATURES

The Get Features command.

### -field NVME_ADMIN_COMMAND_ASYNC_EVENT_REQUEST

The Asynchronous Event Request command.

### -field NVME_ADMIN_COMMAND_NAMESPACE_MANAGEMENT

The Namespace Management command.

### -field NVME_ADMIN_COMMAND_FIRMWARE_ACTIVATE

This command has been renamed to the Firmware Commit command in NVME spec v1.2.

### -field NVME_ADMIN_COMMAND_FIRMWARE_COMMIT

The Firmware Commit command.

### -field NVME_ADMIN_COMMAND_FIRMWARE_IMAGE_DOWNLOAD

The Firmware Image Download command.

### -field NVME_ADMIN_COMMAND_DEVICE_SELF_TEST

The Device Self-test command

### -field NVME_ADMIN_COMMAND_NAMESPACE_ATTACHMENT

The Namespace Attachment command.

### -field NVME_ADMIN_COMMAND_DIRECTIVE_SEND

The Directive Send command.

### -field NVME_ADMIN_COMMAND_DIRECTIVE_RECEIVE

The Directive Receive command.

### -field NVME_ADMIN_COMMAND_VIRTUALIZATION_MANAGEMENT

The Virtualization Management command.

### -field NVME_ADMIN_COMMAND_NVME_MI_SEND

The NVMe-MI Send command

### -field NVME_ADMIN_COMMAND_NVME_MI_RECEIVE

The NVMe-MI Receive command.

### -field NVME_ADMIN_COMMAND_DOORBELL_BUFFER_CONFIG

The Doorbell Buffer Config command.

### -field NVME_ADMIN_COMMAND_FORMAT_NVM

The Format NVM command.

### -field NVME_ADMIN_COMMAND_SECURITY_SEND

The Security Send command.

### -field NVME_ADMIN_COMMAND_SECURITY_RECEIVE

The Security Receive command.

### -field NVME_ADMIN_COMMAND_SANITIZE

The Sanitize command.

## -remarks

## -see-also

