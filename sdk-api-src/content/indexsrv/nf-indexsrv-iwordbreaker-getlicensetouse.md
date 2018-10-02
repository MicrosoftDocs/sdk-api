---
UID: NF:indexsrv.IWordBreaker.GetLicenseToUse
title: IWordBreaker::GetLicenseToUse
author: windows-sdk-content
description: Gets a pointer to the license information for this implementation of the IWordBreaker interface.
old-location: search\_search_IWordBreaker_GetLicenseToUse.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\iwordbreaker\getlicensetouse.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetLicenseToUse, GetLicenseToUse method [search], GetLicenseToUse method [search],IWordBreaker interface, IWordBreaker interface [search],GetLicenseToUse method, IWordBreaker.GetLicenseToUse, IWordBreaker::GetLicenseToUse, _search_IWordBreaker_GetLicenseToUse, indexsrv/IWordBreaker::GetLicenseToUse, search._search_IWordBreaker_GetLicenseToUse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: indexsrv.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Indexsrv.h
api_name:
 - IWordBreaker.GetLicenseToUse
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows NT 4.0 Option Pack
---

# IWordBreaker::GetLicenseToUse


## -description


Gets a pointer to the license information for this implementation of the <a href="https://msdn.microsoft.com/en-us/library/Bb266433(v=VS.85).aspx">IWordBreaker</a> interface.


## -parameters




### -param ppwcsLicense [out]

Type: <b>WCHAR const**</b>

Pointer to a variable that receives a pointer to the license information for this <a href="https://msdn.microsoft.com/en-us/library/Bb266433(v=VS.85).aspx">IWordBreaker</a> implementation.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



