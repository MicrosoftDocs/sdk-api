---
UID: NF:sbe.ISBE2Crossbar.EnumStreams
title: ISBE2Crossbar::EnumStreams
author: windows-sdk-content
description: Gets an enumeration object for all streams that are discovered in a WTV file. The filter crossbar, which exposes the ISBE2Crossbar interface, manages the mappings between the streams in the WTV file and the filter output pins.
old-location: mstv\isbe2crossbar_enumstreams.htm
old-project: mstv
ms.assetid: 891dc676-8930-41bc-a0ae-4a080c6d4cd6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: EnumStreams, EnumStreams method [Microsoft TV Technologies], EnumStreams method [Microsoft TV Technologies],ISBE2Crossbar interface, ISBE2Crossbar interface [Microsoft TV Technologies],EnumStreams method, ISBE2Crossbar.EnumStreams, ISBE2Crossbar::EnumStreams, mstv.isbe2crossbar_enumstreams, sbe/ISBE2Crossbar::EnumStreams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2Crossbar.EnumStreams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISBE2Crossbar::EnumStreams


## -description


Gets an enumeration object for all streams that are discovered in a WTV file. The filter crossbar, which exposes the <a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a> interface, manages the mappings between the streams in the WTV file and the filter output pins.

The WTV file format supports dynamic creation and deletion of streams within the file. An <a href="https://msdn.microsoft.com/ab7ccd5b-1ac8-4d33-aea6-49383025270b">SBE2_STREAM_DESC</a> global spanning event in the file signals when a stream is created or deleted.


## -parameters




### -param ppStreams [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/77a918f8-d305-4d4d-9a5c-523ddb796b26">ISBE2EnumStream</a> interface that the crossbar implements.
          You can use the methods that are defined by the <b>ISBE2EnumStream</b>  interface to enumerate the streams that can be mapped to output pins in the current profile. The caller is responsible for releasing the interface.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_FAIL</dt>
</dl>
</td>
<td width="60%">
No streams found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a>



<a href="https://msdn.microsoft.com/77a918f8-d305-4d4d-9a5c-523ddb796b26">ISBE2EnumStream</a>



<a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source Filter</a>
 

 

