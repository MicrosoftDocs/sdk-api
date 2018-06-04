---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

