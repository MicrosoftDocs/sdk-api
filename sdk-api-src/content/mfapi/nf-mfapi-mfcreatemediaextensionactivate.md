---
UID: NF:mfapi.MFCreateMediaExtensionActivate
title: MFCreateMediaExtensionActivate function
author: windows-sdk-content
description: Creates an activation object for a Windows Runtime class.
old-location: mf\mfcreatemediaextensionactivate.htm
tech.root: medfound
ms.assetid: 3F9538F2-DB7A-4841-B61D-C59BC02718B1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFCreateMediaExtensionActivate, MFCreateMediaExtensionActivate function [Media Foundation], mf.mfcreatemediaextensionactivate, mf.mfcreatewinrtactivate, mfapi/MFCreateMediaExtensionActivate
ms.topic: function
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateMediaExtensionActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateMediaExtensionActivate function


## -description


Creates an activation object for a Windows Runtime class.


## -parameters




### -param szActivatableClassId [in]

The class identifier that is associated with the activatable runtime class.


### -param pConfiguration [in]

A pointer to an optional <a href="https://msdn.microsoft.com/9fd38910-0ee6-4cbd-9dcf-ac7129d2c911">IPropertySet</a> object, which is used to configure the Windows Runtime class. This parameter can be <b>NULL</b>.


### -param riid [in]

The interface identifier (IID) of the interface being requested. The activation object created  by this function supports the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>
</li>
</ul>

### -param ppvObject [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To create the Windows Runtime object, call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> or <a href="https://msdn.microsoft.com/45d34150-9e0b-4a76-a784-c81434ec73b8">IClassFactory::CreateInstance</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

