---
UID: NF:rometadataapi.IMetaDataTables.GetNextGuid
title: IMetaDataTables::GetNextGuid (rometadataapi.h)
description: Gets the index of the next GUID value in the current table column.helpviewer_keywords: ["GetNextGuid","GetNextGuid method [Windows Runtime]","GetNextGuid method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetNextGuid method","IMetaDataTables.GetNextGuid","IMetaDataTables::GetNextGuid","rometadataapi/IMetaDataTables::GetNextGuid","winrt.imetadatatables_getnextguid"]
old-location: winrt\imetadatatables_getnextguid.htm
tech.root: WinRT
ms.assetid: b624f727-8371-49a1-8ec7-7110d9b8f971
ms.date: 12/05/2018
ms.keywords: GetNextGuid, GetNextGuid method [Windows Runtime], GetNextGuid method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetNextGuid method, IMetaDataTables.GetNextGuid, IMetaDataTables::GetNextGuid, rometadataapi/IMetaDataTables::GetNextGuid, winrt.imetadatatables_getnextguid
f1_keywords:
- rometadataapi/IMetaDataTables.GetNextGuid
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- rometadataapi.h
api_name:
- IMetaDataTables.GetNextGuid
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataTables::GetNextGuid


## -description


Gets the index of the next GUID value in the current table column.


## -parameters




### -param ixGuid [in]

The index value from a GUID table column.


### -param pNext [out]

A pointer to the index of the next GUID value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We do not recommend the use of this method, because it does not return consistent results. For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics". The documentation is available online; see <a href="https://docs.microsoft.com/dotnet/standard/components#applicable-standards">ECMA C# and Common Language Infrastructure Standards</a> on MSDN and <a href="https://www.ecma-international.org/publications/standards/Ecma-335.htm">Standard ECMA-335 - Common Language Infrastructure (CLI)</a> on the Ecma International Web site.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>
 

 

