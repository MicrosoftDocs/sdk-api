---
UID: NE:shobjidl_core._SICHINTF
title: "_SICHINTF"
author: windows-sdk-content
description: Used to determine how to compare two Shell items. IShellItem::Compare uses this enumerated type.
old-location: shell\SICHINT.htm
tech.root: shell
ms.assetid: 4d333302-5be3-4e8d-9018-e42729df0cc3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SICHINTF, SICHINTF enumeration [Windows Shell], SICHINT_ALLFIELDS, SICHINT_CANONICAL, SICHINT_DISPLAY, SICHINT_TEST_FILESYSPATH_IF_NOT_EQUAL, _SICHINTF, inet_SICHINT, shell.SICHINT, shobjidl_core/SICHINTF, shobjidl_core/SICHINT_ALLFIELDS, shobjidl_core/SICHINT_CANONICAL, shobjidl_core/SICHINT_DISPLAY, shobjidl_core/SICHINT_TEST_FILESYSPATH_IF_NOT_EQUAL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - SICHINTF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _SICHINTF enumeration


## -description


Used to determine how to compare two Shell items. <a href="https://msdn.microsoft.com/737a93e0-2e27-466b-889c-04a25e52e883">IShellItem::Compare</a> uses this enumerated type.


## -enum-fields




### -field SICHINT_DISPLAY

0x00000000. This relates to the <i>iOrder</i> parameter of the <a href="https://msdn.microsoft.com/737a93e0-2e27-466b-889c-04a25e52e883">IShellItem::Compare</a> interface and indicates that the comparison is based on the display in a folder view.


### -field SICHINT_ALLFIELDS

(int)0x80000000. Exact comparison of two instances of a Shell item.


### -field SICHINT_CANONICAL

0x10000000. This relates to the <i>iOrder</i> parameter of the <a href="https://msdn.microsoft.com/737a93e0-2e27-466b-889c-04a25e52e883">IShellItem::Compare</a> interface and indicates that the comparison is based on a canonical name.


### -field SICHINT_TEST_FILESYSPATH_IF_NOT_EQUAL

0x20000000. <b>Windows 7 and later</b>. If the Shell items are not the same, test the file system paths.

