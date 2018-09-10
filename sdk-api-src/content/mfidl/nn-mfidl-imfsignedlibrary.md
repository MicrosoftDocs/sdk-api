---
UID: NN:mfidl.IMFSignedLibrary
title: IMFSignedLibrary
author: windows-sdk-content
description: Provides a method that allows content protection systems to get the procedure address of a function in the signed library. This method provides the same functionality as GetProcAddress which is not available to Windows Store apps.
old-location: mf\imfsignedlibrary.htm
tech.root: medfound
ms.assetid: 1170fd74-7da4-49a8-b095-dd1572db382d
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFSignedLibrary, IMFSignedLibrary interface [Media Foundation], IMFSignedLibrary interface [Media Foundation],described, mf.imfsignedlibrary, mfidl/IMFSignedLibrary
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSignedLibrary interface


## -description


Provides a method that allows content protection systems to get the procedure address of a function in the signed library.  This method provides the same functionality as <b>GetProcAddress</b> which is not available to Windows Store apps.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSignedLibrary</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSignedLibrary</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d32678b0-422d-4fe8-9bbc-fc203a39fdd5">GetProcedureAddress</a>
</td>
<td align="left" width="63%">
Gets the procedure address of the specified function in the signed library.

</td>
</tr>
</table> 


## -remarks



See  <a href="https://msdn.microsoft.com/979A5FE5-0DED-4C5A-A27D-CDD10A4A8D5C">MFLoadSignedLibrary</a> for an example of how to create and use an <b>IMFSignedLibrary</b> object.




## -see-also




<a href="https://msdn.microsoft.com/979A5FE5-0DED-4C5A-A27D-CDD10A4A8D5C">MFLoadSignedLibrary</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

