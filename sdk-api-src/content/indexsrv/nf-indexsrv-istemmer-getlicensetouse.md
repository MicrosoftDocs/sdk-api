---
UID: NF:indexsrv.IStemmer.GetLicenseToUse
title: IStemmer::GetLicenseToUse
author: windows-sdk-content
description: Gets the license information for this IStemmer implementation.
old-location: search\_search_IStemmer_GetLicenseToUse.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\istemmer\getlicensetouse.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetLicenseToUse, GetLicenseToUse method [search], GetLicenseToUse method [search],IStemmer interface, IStemmer interface [search],GetLicenseToUse method, IStemmer.GetLicenseToUse, IStemmer::GetLicenseToUse, _search_IStemmer_GetLicenseToUse, indexsrv/IStemmer::GetLicenseToUse, search._search_IStemmer_GetLicenseToUse
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: indexsrv.h
req.include-header: 
req.redist: Windows NT 4.0 Option Pack
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
tech.root: 
req.typenames: WORDREP_BREAK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Indexsrv.h
api_name:
 - IStemmer.GetLicenseToUse
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStemmer::GetLicenseToUse


## -description


Gets the license information for this <a href="https://msdn.microsoft.com/1a6e77ec-60f8-4e43-9420-7a6b50152e26">IStemmer</a> implementation.


## -parameters




### -param ppwcsLicense [out]

Type: <b>const WCHAR**</b>

Pointer to a variable that receives a pointer to the license information for this <a href="https://msdn.microsoft.com/1a6e77ec-60f8-4e43-9420-7a6b50152e26">IStemmer</a> implementation.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Windows Search does not enforce license restrictions. The implementation determines the storage method for the license information.



