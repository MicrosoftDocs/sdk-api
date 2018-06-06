---
UID: NF:iads.IDirectorySearch.FreeColumn
title: IDirectorySearch::FreeColumn
author: windows-sdk-content
description: The IDirectorySearch::FreeColumn method releases memory that the IDirectorySearch::GetColumn method allocated for data for the column.
old-location: adsi\idirectorysearch_freecolumn.htm
old-project: ADSI
ms.assetid: 72e75429-d22c-490f-a1f7-d771628067c9
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: FreeColumn, FreeColumn method [ADSI], FreeColumn method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],FreeColumn method, IDirectorySearch.FreeColumn, IDirectorySearch::FreeColumn, _ds_idirectorysearch_freecolumn, adsi.idirectorysearch__freecolumn, adsi.idirectorysearch_freecolumn, iads/IDirectorySearch::FreeColumn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
 - Adsldp.dll
 - Adsldpc.dll
api_name:
 - IDirectorySearch.FreeColumn
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll; Adsldp.dll; Adsldpc.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDirectorySearch::FreeColumn


## -description


The <b>IDirectorySearch::FreeColumn</b> method 
    releases memory that the 
    <a href="https://msdn.microsoft.com/3bcacb24-a4b4-4fad-ab7c-79ef7a67064d">IDirectorySearch::GetColumn</a> method allocated 
    for data for the column.


## -parameters




### -param pSearchColumn [in]

Provides a pointer to the column to be freed.


## -returns



This method returns the standard return values, as well as the following:

For other return values, see <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>



<a href="https://msdn.microsoft.com/3bcacb24-a4b4-4fad-ab7c-79ef7a67064d">IDirectorySearch::GetColumn</a>
 

 

