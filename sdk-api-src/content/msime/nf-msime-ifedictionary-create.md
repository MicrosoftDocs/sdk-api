---
UID: NF:msime.IFEDictionary.Create
title: IFEDictionary::Create
author: windows-sdk-content
description: Creates a new dictionary file.
old-location: intl\ifedictionary_create.htm
old-project: Intl
ms.assetid: 218DEE1C-945A-4CD8-BAD5-12F904FAB2DD
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Create, Create method [Internationalization for Windows Applications], Create method [Internationalization for Windows Applications],IFEDictionary interface, IFEDictionary interface [Internationalization for Windows Applications],Create method, IFEDictionary.Create, IFEDictionary::Create, intl.ifedictionary_create, msime/IFEDictionary::Create
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msime.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: IMEUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFEDictionary.Create
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFEDictionary::Create


## -description


Creates a new dictionary file.


## -parameters




### -param pchDictPath [in]

A <b>NULL</b>-terminated string containing the path and name for the new dictionary file to be created.


### -param pshf [in]

The <a href="https://msdn.microsoft.com/CFFEFEDC-F614-4DD4-B1A1-4D236339E817">IMESHF</a> header for the new dictionary.


## -returns



One of the following:

<ul>
<li><b>S_OK</b></li>
<li><b>IFED_S_EMPTY_DICTIONARY</b></li>
<li><b>E_OUTOFMEMORY</b></li>
<li><b>E_FAIL</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>



<a href="https://msdn.microsoft.com/CFFEFEDC-F614-4DD4-B1A1-4D236339E817">IMESHF</a>
 

 

