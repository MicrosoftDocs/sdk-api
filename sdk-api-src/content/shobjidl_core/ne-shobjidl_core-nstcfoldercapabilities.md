---
UID: NE:shobjidl_core.NSTCFOLDERCAPABILITIES
title: NSTCFOLDERCAPABILITIES
author: windows-sdk-content
description: Specifies the state of a tree item. These values are used by methods of the INameSpaceTreeControlFolderCapabilities interface.
old-location: shell\NSTCFOLDERCAPABILITIES.htm
tech.root: shell
ms.assetid: a5282277-85f5-494e-b994-efbf1116b519
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: NSTCFC_DELAY_REGISTER_NOTIFY, NSTCFC_NONE, NSTCFC_PINNEDITEMFILTERING, NSTCFOLDERCAPABILITIES, NSTCFOLDERCAPABILITIES enumeration [Windows Shell], _shell_NSTCFOLDERCAPABILITIES, shell.NSTCFOLDERCAPABILITIES, shobjidl_core/NSTCFC_DELAY_REGISTER_NOTIFY, shobjidl_core/NSTCFC_NONE, shobjidl_core/NSTCFC_PINNEDITEMFILTERING, shobjidl_core/NSTCFOLDERCAPABILITIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - NSTCFOLDERCAPABILITIES
product: Windows
targetos: Windows
req.typenames: NSTCFOLDERCAPABILITIES
req.redist: 
---

# NSTCFOLDERCAPABILITIES enumeration


## -description


Specifies the state of a tree item. These values are used by methods of the <a href="https://msdn.microsoft.com/2a5580f6-42cb-46c7-9507-a59d36b2cd91">INameSpaceTreeControlFolderCapabilities</a> interface.


## -enum-fields




### -field NSTCFC_NONE

The property does not exist. Filtering is not supported.


### -field NSTCFC_PINNEDITEMFILTERING

Property exists. Supports filtering based on the value specified in <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a>.


### -field NSTCFC_DELAY_REGISTER_NOTIFY

Delays registration for change notifications until the tree is expanded in the navigation pane.


## -remarks



The <b>NSTCFOLDERCAPABILITIES</b> type is defined in Shobjidl.h beginning in Windows 7.




## -see-also




<a href="https://msdn.microsoft.com/1534431c-21fc-4eb9-8f17-ddd7414bef94">INameSpaceTreeControlFolderCapabilities::GetFolderCapabilities</a>
 

 

