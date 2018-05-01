---
UID: NF:mfidl.IMFObjectReferenceStream.SaveReference
title: IMFObjectReferenceStream::SaveReference method
author: windows-driver-content
description: Stores the data needed to marshal an interface across a process boundary.
old-location: mf\imfobjectreferencestream_savereference.htm
old-project: medfound
ms.assetid: 776f94c4-d0e9-4fb7-a39c-32c83428bbe3
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 776f94c4-d0e9-4fb7-a39c-32c83428bbe3, IMFObjectReferenceStream, IMFObjectReferenceStream interface [Media Foundation], SaveReference method, IMFObjectReferenceStream::SaveReference, SaveReference method [Media Foundation], SaveReference method [Media Foundation], IMFObjectReferenceStream interface, SaveReference,IMFObjectReferenceStream.SaveReference, mf.imfobjectreferencestream_savereference, mfidl/IMFObjectReferenceStream::SaveReference
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFObjectReferenceStream.SaveReference
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFObjectReferenceStream::SaveReference method


## -description



Stores the data needed to marshal an interface across a process boundary.




## -parameters




### -param riid [in]

Interface identifier of the interface to marshal.


### -param pUnk [in]

Pointer to the <b>IUnknown</b> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9d29befd-b0ae-4610-a0b7-17face03c45e">IMFObjectReferenceStream</a>
 

 

