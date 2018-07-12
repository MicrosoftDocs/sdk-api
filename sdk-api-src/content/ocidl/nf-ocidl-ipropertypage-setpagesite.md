---
UID: NF:ocidl.IPropertyPage.SetPageSite
title: IPropertyPage::SetPageSite
author: windows-sdk-content
description: Initializes a property page and provides the page with a pointer to the IPropertyPageSite interface through which the property page communicates with the property frame.
old-location: com\ipropertypage_setpagesite.htm
old-project: com
ms.assetid: a57f3f0c-53c0-4ddf-9827-df912f263a9e
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IPropertyPage interface [COM],SetPageSite method, IPropertyPage.SetPageSite, IPropertyPage::SetPageSite, SetPageSite, SetPageSite method [COM], SetPageSite method [COM],IPropertyPage interface, _ctrl_ipropertypage_setpagesite, com.ipropertypage_setpagesite, ocidl/IPropertyPage::SetPageSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyPage.SetPageSite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyPage::SetPageSite


## -description


Initializes a property page and provides the page with a pointer to the <a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a> interface through which the property page communicates with the property frame.


## -parameters




### -param pPageSite [in]

A pointer to the <a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a> interface of the page site that manages and provides services to this property page within the entire property sheet.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the <i>pPageSite</i> parameter is <b>NULL</b>, this method must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on any <a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a> pointer passed during a previous call to this method. If non-<b>NULL</b>, this method must save the <b>IPropertyPageSite</b> pointer value and call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>. Two consecutive calls to this method with a non-<b>NULL</b> site pointer are not allowed and should cause the property page to return E_UNEXPECTED.

E_NOTIMPL is not a valid return value. All property pages must implement this method.




## -see-also




<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>
 

 

