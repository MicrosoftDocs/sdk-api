---
UID: NF:strmif.IPersistMediaPropertyBag.Save
title: IPersistMediaPropertyBag::Save method
author: windows-driver-content
description: The Save method saves properties from the filter into the media property bag.
old-location: dshow\ipersistmediapropertybag_save.htm
old-project: DirectShow
ms.assetid: 12c66650-31c1-40b8-9f3d-bc5553dbfa94
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IPersistMediaPropertyBag, IPersistMediaPropertyBag interface [DirectShow], Save method, IPersistMediaPropertyBag::Save, IPersistMediaPropertyBagSave, Save method [DirectShow], Save method [DirectShow], IPersistMediaPropertyBag interface, Save,IPersistMediaPropertyBag.Save, dshow.ipersistmediapropertybag_save, strmif/IPersistMediaPropertyBag::Save
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IPersistMediaPropertyBag.Save
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IPersistMediaPropertyBag::Save method


## -description



The <code>Save</code> method saves properties from the filter into the media property bag.




## -parameters




### -param pPropBag [in]

Pointer to the <a href="https://msdn.microsoft.com/6f134160-b0aa-44fd-b1b9-938f11349eac">IMediaPropertyBag</a> interface of a media property bag created by the caller.


### -param fClearDirty [in]

Reserved. Can be any value.


### -param fSaveAllProperties [in]

Reserved. Can be any value.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></dt>
</dl>
</td>
<td width="60%">
Invalid data.

</td>
</tr>
</table>
 




## -remarks



If you call this method on the <a href="https://msdn.microsoft.com/df3c7d11-7ecc-499a-af36-b74437e21999">AVI Splitter</a> filter or the <a href="https://msdn.microsoft.com/53a9538d-7a79-40bb-9468-d710eb238925">WAVE Parser</a>, the filter reads any INFO and DISP chunks from the file and stores them in the media property bag. You can use the <a href="https://msdn.microsoft.com/88cd9016-ef6f-467a-9e84-10b2ac578211">IMediaPropertyBag::EnumProperty</a> method to retrieve the chunks.

The <a href="https://msdn.microsoft.com/31d30c91-fc6a-45ec-a2e0-34e6a1e902a4">AVI Mux</a> filter does not implement this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/33e4b76b-841a-4dc5-b117-e08a6f4dcbe7">IPersistMediaPropertyBag Interface</a>
 

 

