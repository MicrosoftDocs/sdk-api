---
UID: NF:dvbsiparser.IIsdbDigitalCopyControlDescriptor.GetTag
title: IIsdbDigitalCopyControlDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.
old-location: mstv\iisdbdigitalcopycontroldescriptor_gettag.htm
tech.root: MSTV
ms.assetid: 9e14cb87-3669-4fdf-9c84-b7f2e3c840c2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbDigitalCopyControlDescriptor interface, IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbDigitalCopyControlDescriptor.GetTag, IIsdbDigitalCopyControlDescriptor::GetTag, dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetTag, mstv.iisdbdigitalcopycontroldescriptor_gettag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbDigitalCopyControlDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IIsdbDigitalCopyControlDescriptor.GetTag
: 
---

# IIsdbDigitalCopyControlDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For a digital copy control descriptor, this value is 0xC1.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d509eb58-0c58-4173-8c9c-d52b81932b5c">IIsdbDigitalCopyControlDescriptor</a>
 

 

