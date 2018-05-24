---
UID: NF:msime.IFEDictionary.Open
title: IFEDictionary::Open
author: windows-driver-content
description: Opens a dictionary file.
old-location: intl\ifedictionary_open.htm
old-project: Intl
ms.assetid: 7170EED5-0D96-4314-8B9F-A019052B0F32
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IFEDictionary interface [Internationalization for Windows Applications],Open method, IFEDictionary.Open, IFEDictionary::Open, Open, Open method [Internationalization for Windows Applications], Open method [Internationalization for Windows Applications],IFEDictionary interface, intl.ifedictionary_open, msime/IFEDictionary::Open
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msime.h
req.include-header: 
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
req.typenames: IMEUCT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msime.h
api_name:
-	IFEDictionary.Open
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFEDictionary::Open


## -description


Opens a dictionary file.

This method opens an existing dictionary file and associates it with this <a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a> object. To implement a multiple dictionary facility, multiple open and release procedures must be carried out.


## -parameters




### -param pchDictPath [in, optional]

Points to a <b>NULL</b>-terminated file name string to be opened. If <i>pchDictPath</i> is <b>NULL</b> or an empty string, the user dictionary opened by the IME kernel will be used. If <i>pchDictPath</i> is an empty string, the name of user dictionary will be copied into <i>pchDictPath</i>, in which case the size of <i>pchDictPath</i> must be <b>MAX_PATH</b>.


### -param pshf [out]

The <a href="https://msdn.microsoft.com/CFFEFEDC-F614-4DD4-B1A1-4D236339E817">IMESHF</a> header of the opened file. Can be <b>NULL</b>.


## -returns



One of the following:

<ul>
<li><b>S_OK</b></li>
<li><b>JDIC_S_EMPTY_DICTIONARY</b></li>
<li><b>IFED_E_NOT_FOUND</b></li>
<li><b>IFED_E_INVALID_FORMAT</b></li>
<li><b>IFED_E_OPEN_FAILED</b></li>
<li><b>E_FAIL</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>



<a href="https://msdn.microsoft.com/CFFEFEDC-F614-4DD4-B1A1-4D236339E817">IMESHF</a>
 

 

