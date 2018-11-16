---
UID: NF:mfidl.IMFSourceResolver.EndCreateObjectFromURL
title: IMFSourceResolver::EndCreateObjectFromURL
author: windows-sdk-content
description: Completes an asynchronous request to create an object from a URL.
old-location: mf\imfsourceresolver_endcreateobjectfromurl.htm
tech.root: medfound
ms.assetid: af50a76d-b083-4815-bbff-820b21ff8d1b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EndCreateObjectFromURL, EndCreateObjectFromURL method [Media Foundation], EndCreateObjectFromURL method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],EndCreateObjectFromURL method, IMFSourceResolver.EndCreateObjectFromURL, IMFSourceResolver::EndCreateObjectFromURL, af50a76d-b083-4815-bbff-820b21ff8d1b, mf.imfsourceresolver_endcreateobjectfromurl, mfidl/IMFSourceResolver::EndCreateObjectFromURL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSourceResolver.EndCreateObjectFromURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFSourceResolver.EndCreateObjectFromURL
: 
---

# IMFSourceResolver::EndCreateObjectFromURL


## -description


Completes an asynchronous request to create an object from a URL.
        


## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">Invoke</a> method.
          


### -param pObjectType [out]

Receives a member of the <a href="https://msdn.microsoft.com/e919ae78-e3a5-42c5-b4e0-186e7e4fe54a">MF_OBJECT_TYPE</a> enumeration, specifying the type of object that was created.
          


### -param ppObject [out]

Receives a pointer to the media source's <b>IUnknown</b> interface. The caller must release the interface.
          


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
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled.
              

</td>
</tr>
</table>
 




## -remarks



Call this method from inside your application's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.




## -see-also




<a href="https://msdn.microsoft.com/079c61c5-7a29-4411-840e-9349190726ac">IMFSourceResolver</a>



<a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a>
 

 

