---
UID: NE:processsnapshot.PSS_HANDLE_FLAGS
title: PSS_HANDLE_FLAGS
author: windows-sdk-content
description: Flags to specify what parts of a PSS_HANDLE_ENTRY structure are valid.
old-location: proc_snap\pss_handle_flags.htm
old-project: proc_snap
ms.assetid: A4A604A9-0210-413C-BCAC-F8458B371D42
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: PSS_HANDLE_FLAGS, PSS_HANDLE_FLAGS enumeration, PSS_HANDLE_HAVE_BASIC_INFORMATION, PSS_HANDLE_HAVE_NAME, PSS_HANDLE_HAVE_TYPE, PSS_HANDLE_HAVE_TYPE_SPECIFIC_INFORMATION, PSS_HANDLE_NONE, proc_snap.pss_handle_flags, processsnapshot/PSS_HANDLE_FLAGS, processsnapshot/PSS_HANDLE_HAVE_BASIC_INFORMATION, processsnapshot/PSS_HANDLE_HAVE_NAME, processsnapshot/PSS_HANDLE_HAVE_TYPE, processsnapshot/PSS_HANDLE_HAVE_TYPE_SPECIFIC_INFORMATION, processsnapshot/PSS_HANDLE_NONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: processsnapshot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PSS_HANDLE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	processsnapshot.h
api_name:
-	PSS_HANDLE_FLAGS
product: Windows
targetos: Windows
req.lib: Prntvpt.lib
req.dll: Prntvpt.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSS_HANDLE_FLAGS enumeration


## -description


Flags to specify what parts of a <a href="https://msdn.microsoft.com/F56E8C35-949A-4DEE-973F-CF24F6596036">PSS_HANDLE_ENTRY</a> structure are valid.


## -enum-fields




### -field PSS_HANDLE_NONE

No parts specified.


### -field PSS_HANDLE_HAVE_TYPE

The <b>ObjectType</b> member is valid.


### -field PSS_HANDLE_HAVE_NAME

The <b>ObjectName</b> member is valid.


### -field PSS_HANDLE_HAVE_BASIC_INFORMATION

The <b>Attributes</b>, <b>GrantedAccess</b>, <b>HandleCount</b>, <b>PointerCount</b>, <b>PagedPoolCharge</b>, and <b>NonPagedPoolCharge</b> members are valid.


### -field PSS_HANDLE_HAVE_TYPE_SPECIFIC_INFORMATION

The <b>TypeSpecificInformation</b> member is valid (either <b>Process</b>, <b>Thread</b>, <b>Mutant</b>, <b>Event</b> or <b>Section</b>).


## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

