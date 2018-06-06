---
UID: NF:rometadataapi.IMetaDataTables.GetGuid
title: IMetaDataTables::GetGuid
author: windows-sdk-content
description: Gets a GUID from the row at the specified index.
old-location: winrt\imetadatatables_getguid.htm
old-project: WinRT
ms.assetid: 037d722f-3efb-4c01-8445-b23caafbbdb2
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: GetGuid, GetGuid method [Windows Runtime], GetGuid method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetGuid method, IMetaDataTables.GetGuid, IMetaDataTables::GetGuid, rometadataapi/IMetaDataTables::GetGuid, winrt.imetadatatables_getguid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataTables.GetGuid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataTables::GetGuid


## -description


Gets a GUID from the row at the specified index.


## -parameters




### -param ixGuid [in]

The index of the row from which to get the GUID.


### -param ppGUID [out]

A pointer to a pointer to the GUID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We do not recommend the use of this method, because it does not return consistent results. For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics". The documentation is available online; see <a href="http://go.microsoft.com/fwlink/p/?linkid=199862">ECMA C# and Common Language Infrastructure Standards</a> on MSDN and <a href="http://go.microsoft.com/fwlink/p/?linkid=65552">Standard ECMA-335 - Common Language Infrastructure (CLI)</a> on the Ecma International Web site.




## -see-also




<a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a>
 

 

