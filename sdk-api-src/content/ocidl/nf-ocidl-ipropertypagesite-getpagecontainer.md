---
UID: NF:ocidl.IPropertyPageSite.GetPageContainer
title: IPropertyPageSite::GetPageContainer
author: windows-sdk-content
description: Retrieves a pointer to the object representing the entire property frame dialog box that contains all the pages. Calling this method could potentially allow one page to navigate to another.
old-location: com\ipropertypagesite_getpagecontainer.htm
tech.root: com
ms.assetid: 88cbefe6-51c7-4c09-80bb-677c83f97cac
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetPageContainer, GetPageContainer method [COM], GetPageContainer method [COM],IPropertyPageSite interface, IPropertyPageSite interface [COM],GetPageContainer method, IPropertyPageSite.GetPageContainer, IPropertyPageSite::GetPageContainer, _ctrl_ipropertypagesite_getpagecontainer, com.ipropertypagesite_getpagecontainer, ocidl/IPropertyPageSite::GetPageContainer
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPropertyPageSite.GetPageContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyPageSite::GetPageContainer


## -description


Retrieves a pointer to the object representing the entire property frame dialog box that contains all the pages. Calling this method could potentially allow one page to navigate to another.

However, there are no container interfaces defined for this role, so this method always fails in the property frame implementation.


## -parameters




### -param ppUnk [out]

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer variable that receives the interface pointer to the container object. If an error occurs, the implementation must set *<i>ppUnk</i> to <b>NULL</b>.


## -returns



This method returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a>
 

 

