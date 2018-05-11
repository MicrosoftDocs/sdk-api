---
UID: NF:mfidl.IMFMediaTypeHandler.SetCurrentMediaType
title: IMFMediaTypeHandler::SetCurrentMediaType
author: windows-driver-content
description: Sets the object's media type.
old-location: mf\imfmediatypehandler_setcurrentmediatype.htm
old-project: medfound
ms.assetid: 77ff397e-4fa8-4849-98b8-6bdd035c0e89
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 77ff397e-4fa8-4849-98b8-6bdd035c0e89, IMFMediaTypeHandler interface [Media Foundation],SetCurrentMediaType method, IMFMediaTypeHandler.SetCurrentMediaType, IMFMediaTypeHandler::SetCurrentMediaType, SetCurrentMediaType, SetCurrentMediaType method [Media Foundation], SetCurrentMediaType method [Media Foundation],IMFMediaTypeHandler interface, mf.imfmediatypehandler_setcurrentmediatype, mfidl/IMFMediaTypeHandler::SetCurrentMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
-	IMFMediaTypeHandler.SetCurrentMediaType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaTypeHandler::SetCurrentMediaType


## -description



Sets the object's media type.




## -parameters




### -param pMediaType [in]

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the new media type.


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">

                Invalid request.
              

</td>
</tr>
</table>
 




## -remarks



For media sources, setting the media type means the source will generate data that conforms to that media type. For media sinks, setting the media type means the sink can receive data that conforms to that media type.

Any implementation of this method should check whether <i>pMediaType</i> differs from the object's current media type. If the types are identical, the method should return S_OK but avoid releasing and recreating resources unnecessarily. If the types are not identical, the method should validate the new type.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a>
 

 

