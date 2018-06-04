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

# IInkEdit::get_InkMode


## -description



Gets or sets a value that specifies whether ink collection is disabled, ink is collected, or ink and gestures are collected.



This property is read/write.


## -parameters


## -remarks



The value of this property is always Disabled if it is used on a system that has Microsoft Windows XP Tablet PC Edition installed but no recognizers are present. If used on a system with Windows Vista or Windows XP Tablet PC Edition installed, the value can be set to any of the values in the <a href="https://msdn.microsoft.com/81aac302-c89a-42ca-9c90-170611a8995a">InkMode</a> enumeration type.

This property should be changed only if the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property returns IES_Idle.




## -see-also




<a href="tablet.iinkedit_">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>



<a href="https://msdn.microsoft.com/81aac302-c89a-42ca-9c90-170611a8995a">InkMode Enumeration</a>
 

 

