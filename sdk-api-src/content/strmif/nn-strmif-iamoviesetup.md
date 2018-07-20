---
UID: NN:strmif.IAMovieSetup
title: IAMovieSetup
author: windows-sdk-content
description: Note  This interface has been deprecated.
old-location: dshow\iamoviesetup.htm
old-project: DirectShow
ms.assetid: b200dbee-bab7-43d7-a204-751592fa2405
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IAMovieSetup, IAMovieSetup interface [DirectShow], IAMovieSetup interface [DirectShow],described, IAMovieSetupInterface, dshow.iamoviesetup, strmif/IAMovieSetup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IAMovieSetup
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMovieSetup interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. It is used by two obsolete functions, <a href="https://msdn.microsoft.com/d3be5fe0-f993-4a15-a3b8-3d761d51f289">AMovieDllRegisterServer</a> and <a href="https://msdn.microsoft.com/80f52109-6239-4e3d-a395-eb69f5278cd2">AMovieDllUnregisterServer</a>. These functions are now replaced by <a href="https://msdn.microsoft.com/2122949d-0117-4c68-bfcd-c717b14dc970">AMovieDllRegisterServer2</a>, which does not require <b>IAMovieSetup</b>. However, <b>IAMovieSetup</b> will continue to be supported for backward compatibility with existing applications.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMovieSetup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMovieSetup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMovieSetup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c39edba2-df48-43e4-9a0d-d5c409a8a9d0">Register</a>
</td>
<td align="left" width="63%">
Adds the filter to the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96266aef-f1ef-4b75-9d2e-e574f76fdec7">Unregister</a>
</td>
<td align="left" width="63%">
Removes the filter from the registry.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

