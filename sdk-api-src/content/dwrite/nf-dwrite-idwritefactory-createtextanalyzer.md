---
UID: NF:dwrite.IDWriteFactory.CreateTextAnalyzer
title: IDWriteFactory::CreateTextAnalyzer
author: windows-sdk-content
description: Returns an interface for performing text analysis.
old-location: directwrite\IDWriteFactory_CreateTextAnalyzer.htm
tech.root: DirectWrite
ms.assetid: 1f786de4-9498-49ef-b884-7e5f69cefe4a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateTextAnalyzer, CreateTextAnalyzer method [Direct Write], CreateTextAnalyzer method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateTextAnalyzer method, IDWriteFactory.CreateTextAnalyzer, IDWriteFactory::CreateTextAnalyzer, directwrite.IDWriteFactory_CreateTextAnalyzer, dwrite/IDWriteFactory::CreateTextAnalyzer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory.CreateTextAnalyzer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteFactory.CreateTextAnalyzer
: 
---

# IDWriteFactory::CreateTextAnalyzer


## -description


 Returns an interface for performing text analysis.


## -parameters




### -param textAnalyzer [out]

Type: <b><a href="https://msdn.microsoft.com/e832ffc4-31db-41b1-a008-04696d9a975e">IDWriteTextAnalyzer</a>**</b>

When this method returns, contains an address of  a pointer to the newly created text analyzer object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

