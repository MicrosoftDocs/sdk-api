---
UID: NF:shcore.CreateRandomAccessStreamOnFile
title: CreateRandomAccessStreamOnFile function
author: windows-sdk-content
description: Creates a Windows Runtime random access stream for a file.
old-location: winrt\createrandomaccessstreamonfile.htm
old-project: WinRT
ms.assetid: 6D3D2B25-7373-4BA5-BF6B-FB461C2DE982
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: CreateRandomAccessStreamOnFile, CreateRandomAccessStreamOnFile function [Windows Runtime], shcore/CreateRandomAccessStreamOnFile, winrt.createrandomaccessstreamonfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shcore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: BSOS_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	shcore.dll
-	API-MS-Win-ShCore-stream-WinRT-l1-1-0.dll
api_name:
-	CreateRandomAccessStreamOnFile
product: Windows
targetos: Windows
req.lib: Shcore.lib
req.dll: Shcore.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CreateRandomAccessStreamOnFile function


## -description


Creates a  Windows Runtime random access stream for a file.


## -parameters




### -param filePath [in]

The fully qualified path of the file to encapsulate.


### -param accessMode [in]

An <a href="https://msdn.microsoft.com/2905de68-84f9-4cc1-9389-8ec611b1eece">AccessMode</a> value that specifies the behavior of the <a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a> that encapsulates the file.


### -param riid [in]

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_RandomAccessStream.


### -param ppv [out]

When this method returns successfully, contains the interface pointer requested in <i>riid</i>, typically the <a href="https://msdn.microsoft.com/D2ECEB3D-D13E-44C1-BFE2-1AA57F7432C6">IRandomAccessStream</a> that encapsulates the file.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use the <b>CreateRandomAccessStreamOnFile</b> function to create a <a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a> that encapsulates a file.

We recommend that you use the <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.




## -see-also




<a href="https://msdn.microsoft.com/7A4BA702-0E2E-4FA9-8BEB-313D2D29762E">CreateRandomAccessStreamOverStream</a>



<a href="https://msdn.microsoft.com/F9AB8A34-8AB1-4EF1-8659-DAD5713A89BF">CreateStreamOverRandomAccessStream</a>



<a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a>
 

 

