---
UID: NF:segment.IMSVidFeatures.get__NewEnum
title: IMSVidFeatures::get__NewEnum
author: windows-sdk-content
description: The get__NewEnum method retrieves an enumerator for the collection.
old-location: mstv\imsvidfeatures_get__newenum.htm
tech.root: MSTV
ms.assetid: 6c619f62-5041-410b-8ce0-d811992a32d6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidFeatures interface [Microsoft TV Technologies],get__NewEnum method, IMSVidFeatures.get__NewEnum, IMSVidFeatures::get__NewEnum, IMSVidFeaturesget__NewEnum, get__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies],IMSVidFeatures interface, mstv.imsvidfeatures_get__newenum, segment/IMSVidFeatures::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidFeatures.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidFeatures.get__NewEnum
: 
---

# IMSVidFeatures::get__NewEnum


## -description


The <b>get__NewEnum</b> method retrieves an enumerator for the collection.


## -parameters




### -param pD

TBD




#### - ppD [out]

Pointer to a variable that receives an <b>IEnumVARIANT</b> interface pointer.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method is provided so that Automation clients can iterate through the collection using a <code>For...Each</code> loop.

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread. (C++ applications should generally use the <a href="https://msdn.microsoft.com/f5656ba2-7ba6-44ba-bcab-3678fbd10b07">IMSVidFeatures::get_Item</a> method instead.)

If the method succeeds, the <b>IEnumVARIANT</b> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/19790fab-0530-4a17-8a3c-a50576fea9ca">IMSVidFeatures Interface</a>
 

 

