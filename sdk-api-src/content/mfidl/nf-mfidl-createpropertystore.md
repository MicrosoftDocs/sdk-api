---
UID: NF:mfidl.CreatePropertyStore
title: CreatePropertyStore function
author: windows-driver-content
description: Creates an empty property store object.
old-location: mf\createpropertystore.htm
old-project: medfound
ms.assetid: bb0d32ef-ec16-4341-8b66-d57ebec785f9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CreatePropertyStore, CreatePropertyStore function [Media Foundation], bb0d32ef-ec16-4341-8b66-d57ebec785f9, mf.createpropertystore, mfidl/CreatePropertyStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	CreatePropertyStore
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# CreatePropertyStore function


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Instead, applications should use the <b>PSCreateMemoryPropertyStore</b> function to create property stores.]


          Creates an empty property store object.


## -parameters




### -param ppStore [out]


            Receives a pointer to the <b>IPropertyStore</b> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

