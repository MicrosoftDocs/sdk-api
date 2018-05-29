---
UID: NF:wincodecsdk.WICSerializeMetadataContent
title: WICSerializeMetadataContent function
author: windows-sdk-content
description: Writes metadata into a given stream.
old-location: wic\_wic_codec_wicserializemetadatacontent.htm
old-project: wic
ms.assetid: 726b5e83-d5ab-4053-8f4c-34826fc0db55
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WICSerializeMetadataContent, WICSerializeMetadataContent function [Windows Imaging Component], _wic_codec_wicserializemetadatacontent, wic._wic_codec_wicserializemetadatacontent, wincodecsdk/WICSerializeMetadataContent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincodecsdk.h
req.include-header: Wincodec.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICPersistOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Windowscodecs.dll
-	Wincodec.lib
api_name:
-	WICSerializeMetadataContent
product: Windows
targetos: Windows
req.lib: 
req.dll: Windowscodecs.dll; Wincodec.lib
req.irql: 
req.product: Windows Address Book 5.0
---

# WICSerializeMetadataContent function


## -description


Writes metadata into a given stream.


## -parameters




### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The container format GUID.


### -param pIWriter [in]

Type: <b><a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a>*</b>

The metadata writer to write metadata to the stream.


### -param dwPersistOptions [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/8c17cfcc-4f09-4cb5-a3fa-4eb865123ad6">WICPersistOptions</a> options to use when writing the metadata.


### -param pIStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to the stream in which to write the metadata.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



