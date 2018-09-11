---
UID: NF:strmif.IPersistMediaPropertyBag.InitNew
title: IPersistMediaPropertyBag::InitNew
author: windows-sdk-content
description: The InitNew method initializes the object to receive new properties.
old-location: dshow\ipersistmediapropertybag_initnew.htm
tech.root: DirectShow
ms.assetid: 46d51c05-b653-4f14-810a-eb49d33da359
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IPersistMediaPropertyBag interface [DirectShow],InitNew method, IPersistMediaPropertyBag.InitNew, IPersistMediaPropertyBag::InitNew, IPersistMediaPropertyBagInitNew, InitNew, InitNew method [DirectShow], InitNew method [DirectShow],IPersistMediaPropertyBag interface, dshow.ipersistmediapropertybag_initnew, strmif/IPersistMediaPropertyBag::InitNew
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IPersistMediaPropertyBag.InitNew
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistMediaPropertyBag::InitNew


## -description



The <code>InitNew</code> method initializes the object to receive new properties.




## -parameters






## -returns



Returns S_OK.




## -remarks



Calling this method on the <a href="https://msdn.microsoft.com/31d30c91-fc6a-45ec-a2e0-34e6a1e902a4">AVI Mux</a> filter clears any properties that were previously set using the <a href="https://msdn.microsoft.com/02ee3911-0b85-404d-81c9-7d0e6b3ccd5d">Load</a> method.

Calling this method on the <a href="https://msdn.microsoft.com/df3c7d11-7ecc-499a-af36-b74437e21999">AVI Splitter</a> filter or the <a href="https://msdn.microsoft.com/53a9538d-7a79-40bb-9468-d710eb238925">WAVE Parser</a> filter has no effect.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/33e4b76b-841a-4dc5-b117-e08a6f4dcbe7">IPersistMediaPropertyBag Interface</a>
 

 

