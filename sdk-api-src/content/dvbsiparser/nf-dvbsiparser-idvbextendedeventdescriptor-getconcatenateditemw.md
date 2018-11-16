---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetConcatenatedItemW
title: IDvbExtendedEventDescriptor::GetConcatenatedItemW
author: windows-sdk-content
description: Concatenates the bytes from the item in the current Digital Video Broadcast (DVB) extended event descriptor with the bytes from the item in the next DVB extended event descriptor and returns the concatenated data as a Unicode string.
old-location: mstv\idvbextendedeventdescriptor_getconcatenateditemw.htm
tech.root: mstv
ms.assetid: 9b90a2de-8447-4038-9a11-1db74ebd2feb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetConcatenatedItemW, GetConcatenatedItemW method [Microsoft TV Technologies], GetConcatenatedItemW method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetConcatenatedItemW method, IDvbExtendedEventDescriptor.GetConcatenatedItemW, IDvbExtendedEventDescriptor::GetConcatenatedItemW, dvbsiparser/IDvbExtendedEventDescriptor::GetConcatenatedItemW, mstv.idvbextendedeventdescriptor_getconcatenateditemw
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
 - IDvbExtendedEventDescriptor.GetConcatenatedItemW
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
- IDvbExtendedEventDescriptor.GetConcatenatedItemW
: 
---

# IDvbExtendedEventDescriptor::GetConcatenatedItemW


## -description


Concatenates the bytes from the item in the current Digital Video Broadcast (DVB) extended event descriptor with the bytes from the item in the next DVB extended event descriptor and returns the concatenated data as a Unicode string.


## -parameters




### -param pFollowingDescriptor [in]

Pointer to the <a href="https://msdn.microsoft.com/db100f17-f7b8-4252-8090-44567ab9dcbe">IDvbExtendedEventDescriptor</a> interface for the next DVB extended event descriptor associated with the current one.


### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrDesc [out]

Pointer to a buffer that receives the concatenated item descriptor. The caller is responsible for freeing this memory.


### -param pbstrItem [out]

Pointer to a buffer that receives the concatenated item string. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/db100f17-f7b8-4252-8090-44567ab9dcbe">IDvbExtendedEventDescriptor</a>
 

 

