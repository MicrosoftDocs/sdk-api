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

# tagLVFOOTERINFO structure


## -description


Contains information on a footer in a list-view control.


## -struct-fields




### -field mask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Set of flags that specify which members of this structure contain data to be set or which members are being requested. Currently, this value must be LVFF_ITEMCOUNT, for the <b>cItems</b> member.


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Not supported. Must be set to zero.


### -field cchTextMax

Type: <b>int</b>

Not supported. Must be set to zero.


### -field cItems

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of items in the footer. When this structure is used to get information, this member will be set by the message receiver.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/941d86d8-96f4-4eeb-83b2-c00b279a2cc2">ListView_GetFooterInfo</a> macro and the <a href="https://msdn.microsoft.com/5734e151-50c0-46df-8f2c-220c4910a590">LVM_GETFOOTERINFO</a> message.

The creation of footers in list-view controls is currently not supported.



