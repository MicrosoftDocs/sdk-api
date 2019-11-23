---
UID: NN:mfidl.IMFSignedLibrary
title: IMFSignedLibrary (mfidl.h)

description: Provides a method that allows content protection systems to get the procedure address of a function in the signed library. This method provides the same functionality as GetProcAddress which is not available to Windows Store apps.
old-location: mf\imfsignedlibrary.htm
tech.root: medfound
ms.assetid: 1170fd74-7da4-49a8-b095-dd1572db382d

ms.date: 12/05/2018
ms.keywords: IMFSignedLibrary, IMFSignedLibrary interface [Media Foundation], IMFSignedLibrary interface [Media Foundation],described, mf.imfsignedlibrary, mfidl/IMFSignedLibrary
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFSignedLibrary"
dev_langs:
 - c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - IMFSignedLibrary
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSignedLibrary interface


## -description


Provides a method that allows content protection systems to get the procedure address of a function in the signed library.  This method provides the same functionality as <b>GetProcAddress</b> which is not available to Windows Store apps.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSignedLibrary</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSignedLibrary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSignedLibrary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsignedlibrary-getprocedureaddress">GetProcedureAddress</a>
</td>
<td align="left" width="63%">
Gets the procedure address of the specified function in the signed library.

</td>
</tr>
</table> 


## -remarks



See  <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfloadsignedlibrary">MFLoadSignedLibrary</a> for an example of how to create and use an <b>IMFSignedLibrary</b> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfloadsignedlibrary">MFLoadSignedLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

