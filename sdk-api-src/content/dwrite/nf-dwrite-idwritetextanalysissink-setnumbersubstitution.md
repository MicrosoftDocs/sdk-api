---
UID: NF:dwrite.IDWriteTextAnalysisSink.SetNumberSubstitution
title: IDWriteTextAnalysisSink::SetNumberSubstitution
author: windows-sdk-content
description: Sets the number substitution on the text range affected by the text analysis.
old-location: directwrite\idwritetextanalysissink_setnumbersubstitution.htm
tech.root: DirectWrite
ms.assetid: 09b00b49-702e-4cef-bf1c-397c5d572513
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDWriteTextAnalysisSink interface [Direct Write],SetNumberSubstitution method, IDWriteTextAnalysisSink.SetNumberSubstitution, IDWriteTextAnalysisSink::SetNumberSubstitution, SetNumberSubstitution, SetNumberSubstitution method [Direct Write], SetNumberSubstitution method [Direct Write],IDWriteTextAnalysisSink interface, directwrite.idwritetextanalysissink_setnumbersubstitution, dwrite/IDWriteTextAnalysisSink::SetNumberSubstitution
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
 - IDWriteTextAnalysisSink.SetNumberSubstitution
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalysisSink::SetNumberSubstitution


## -description


Sets the number substitution on the text range affected by the text analysis.


## -parameters




### -param textPosition

Type: <b>UINT32</b>

The starting position from which to report.


### -param textLength

Type: <b>UINT32</b>

The number of UTF16 units of the reported range.


### -param numberSubstitution

Type: <b><a href="https://msdn.microsoft.com/bf8caeea-6ede-4cd3-84f7-2e8314af50db">IDWriteNumberSubstitution</a>*</b>

An object that holds the appropriate digits and numeric punctuation for a given locale. Use <a href="https://msdn.microsoft.com/a2778bfd-c721-44e8-ac0a-79aaa2b323a8">IDWriteFactory::CreateNumberSubstitution</a> to create this object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1fd2ca46-006c-4b01-8258-6c24f4be1641">IDWriteTextAnalysisSink</a>
 

 

