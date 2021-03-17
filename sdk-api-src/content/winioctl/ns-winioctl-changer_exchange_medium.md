---
UID: NS:winioctl._CHANGER_EXCHANGE_MEDIUM
title: CHANGER_EXCHANGE_MEDIUM
description: Contains information the IOCTL_CHANGER_EXCHANGE_MEDIUM control code uses to move a piece of media to a destination, and the piece of media originally in the first destination to a second destination.
helpviewer_keywords: ["*PCHANGER_EXCHANGE_MEDIUM","CHANGER_EXCHANGE_MEDIUM","CHANGER_EXCHANGE_MEDIUM structure","PCHANGER_EXCHANGE_MEDIUM","PCHANGER_EXCHANGE_MEDIUM structure pointer","_win32_changer_exchange_medium_str","base.changer_exchange_medium_str","winioctl/CHANGER_EXCHANGE_MEDIUM","winioctl/PCHANGER_EXCHANGE_MEDIUM"]
old-location: base\changer_exchange_medium_str.htm
tech.root: base
ms.assetid: a35c9da8-7632-4aa1-a1a7-030ffce727b7
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_EXCHANGE_MEDIUM, CHANGER_EXCHANGE_MEDIUM, CHANGER_EXCHANGE_MEDIUM structure, PCHANGER_EXCHANGE_MEDIUM, PCHANGER_EXCHANGE_MEDIUM structure pointer, _win32_changer_exchange_medium_str, base.changer_exchange_medium_str, winioctl/CHANGER_EXCHANGE_MEDIUM, winioctl/PCHANGER_EXCHANGE_MEDIUM'
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
targetos: Windows
req.typenames: CHANGER_EXCHANGE_MEDIUM, *PCHANGER_EXCHANGE_MEDIUM
req.redist: 
f1_keywords:
 - _CHANGER_EXCHANGE_MEDIUM
 - winioctl/_CHANGER_EXCHANGE_MEDIUM
 - PCHANGER_EXCHANGE_MEDIUM
 - winioctl/PCHANGER_EXCHANGE_MEDIUM
 - CHANGER_EXCHANGE_MEDIUM
 - winioctl/CHANGER_EXCHANGE_MEDIUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CHANGER_EXCHANGE_MEDIUM
---

# CHANGER_EXCHANGE_MEDIUM structure


## -description

Contains information the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_exchange_medium">IOCTL_CHANGER_EXCHANGE_MEDIUM</a> control code uses to move a piece of media to a destination, and the piece of media originally in the first destination to a second destination.

## -struct-fields

### -field Transport

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that indicates which transport element to use for the exchange operation. The <b>ElementType</b> member of this structure must be ChangerTransport.

### -field Source

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that indicates the element that contains the media that is to be moved.

### -field Destination1

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that indicates the element that is the destination of the media originally at <b>Source</b>.

### -field Destination2

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that indicates the element that is the destination of the media originally at <b>Destination1</b>.

### -field Flip1

If this member is <b>TRUE</b>, the medium at <b>Destination1</b> should be flipped. Otherwise, it should not. This member is valid only if the <b>Features0</b> member of the 
<a href="/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a> structure is CHANGER_MEDIUM_FLIP.

### -field Flip2

If this member is <b>TRUE</b>, the medium at <b>Destination2</b> should be flipped. Otherwise, it should not. This member is valid only if the <b>Features0</b> member of the 
<a href="/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a> structure is CHANGER_MEDIUM_FLIP.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_exchange_medium">IOCTL_CHANGER_EXCHANGE_MEDIUM</a>