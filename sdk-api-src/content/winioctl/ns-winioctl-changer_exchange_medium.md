---
UID: NS:winioctl._CHANGER_EXCHANGE_MEDIUM
title: CHANGER_EXCHANGE_MEDIUM
author: windows-sdk-content
description: Contains information the IOCTL_CHANGER_EXCHANGE_MEDIUM control code uses to move a piece of media to a destination, and the piece of media originally in the first destination to a second destination.
old-location: base\changer_exchange_medium_str.htm
tech.root: devio
ms.assetid: a35c9da8-7632-4aa1-a1a7-030ffce727b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCHANGER_EXCHANGE_MEDIUM, CHANGER_EXCHANGE_MEDIUM, CHANGER_EXCHANGE_MEDIUM structure, PCHANGER_EXCHANGE_MEDIUM, PCHANGER_EXCHANGE_MEDIUM structure pointer, _win32_changer_exchange_medium_str, base.changer_exchange_medium_str, winioctl/CHANGER_EXCHANGE_MEDIUM, winioctl/PCHANGER_EXCHANGE_MEDIUM"
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - WinIoCtl.h
api_name:
 - CHANGER_EXCHANGE_MEDIUM
product: Windows
targetos: Windows
req.typenames: CHANGER_EXCHANGE_MEDIUM, *PCHANGER_EXCHANGE_MEDIUM
req.redist: 
---

# CHANGER_EXCHANGE_MEDIUM structure


## -description


Contains information the 
<a href="https://msdn.microsoft.com/40550df0-9da4-4b02-bd57-23eae78c68df">IOCTL_CHANGER_EXCHANGE_MEDIUM</a> control code uses to move a piece of media to a destination, and the piece of media originally in the first destination to a second destination.


## -struct-fields




### -field Transport

A 
<a href="https://msdn.microsoft.com/96e9803b-16c4-415c-940a-f5df3edff3b3">CHANGER_ELEMENT</a> structure that indicates which transport element to use for the exchange operation. The <b>ElementType</b> member of this structure must be ChangerTransport.


### -field Source

A 
<a href="https://msdn.microsoft.com/96e9803b-16c4-415c-940a-f5df3edff3b3">CHANGER_ELEMENT</a> structure that indicates the element that contains the media that is to be moved.


### -field Destination1

A 
<a href="https://msdn.microsoft.com/96e9803b-16c4-415c-940a-f5df3edff3b3">CHANGER_ELEMENT</a> structure that indicates the element that is the destination of the media originally at <b>Source</b>.


### -field Destination2

A 
<a href="https://msdn.microsoft.com/96e9803b-16c4-415c-940a-f5df3edff3b3">CHANGER_ELEMENT</a> structure that indicates the element that is the destination of the media originally at <b>Destination1</b>.


### -field Flip1

If this member is <b>TRUE</b>, the medium at <b>Destination1</b> should be flipped. Otherwise, it should not. This member is valid only if the <b>Features0</b> member of the 
<a href="https://msdn.microsoft.com/ad5b6cc3-19f1-4196-9f03-791f342d0cf9">GET_CHANGER_PARAMETERS</a> structure is CHANGER_MEDIUM_FLIP.


### -field Flip2

If this member is <b>TRUE</b>, the medium at <b>Destination2</b> should be flipped. Otherwise, it should not. This member is valid only if the <b>Features0</b> member of the 
<a href="https://msdn.microsoft.com/ad5b6cc3-19f1-4196-9f03-791f342d0cf9">GET_CHANGER_PARAMETERS</a> structure is CHANGER_MEDIUM_FLIP.


## -see-also




<a href="https://msdn.microsoft.com/96e9803b-16c4-415c-940a-f5df3edff3b3">CHANGER_ELEMENT</a>



<a href="https://msdn.microsoft.com/40550df0-9da4-4b02-bd57-23eae78c68df">IOCTL_CHANGER_EXCHANGE_MEDIUM</a>
 

 

