---
UID: NF:ocidl.IObjectWithSite.SetSite
title: IObjectWithSite::SetSite (ocidl.h)
author: windows-sdk-content
description: Enables a container to pass an object a pointer to the interface for its site.
old-location: com\iobjectwithsite_setsite.htm
tech.root: com
ms.assetid: 5e95b2a6-85b3-4899-9e23-54ed9e69e821
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IObjectWithSite interface [COM],SetSite method, IObjectWithSite.SetSite, IObjectWithSite::SetSite, SetSite, SetSite method [COM], SetSite method [COM],IObjectWithSite interface, _ole_iobjectwithsite_setsite, com.iobjectwithsite_setsite, ocidl/IObjectWithSite::SetSite
ms.topic: method
f1_keywords: 
 - "ocidl/IObjectWithSite.SetSite"
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IObjectWithSite.SetSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectWithSite::SetSite


## -description


Enables a container to pass an object a pointer to the interface for its site.


## -parameters




### -param pUnkSite [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer of the site managing this object. If <b>NULL</b>, the object should call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on any existing site at which point the object no longer knows its site.


## -returns



This method returns S_OK on success.




## -remarks



The object should hold onto this pointer, calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> in doing so. If the object already has a site, it should call that existing site's <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>, save the new site pointer, and call the new site's <b>IUnknown::AddRef</b>.

E_NOTIMPL is not allowedâ€”without implementation of the <b>SetSite</b> method, the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a> interface is unnecessary.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a>
 

 

