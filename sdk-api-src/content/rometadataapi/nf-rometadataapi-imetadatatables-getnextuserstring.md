---
UID: NF:rometadataapi.IMetaDataTables.GetNextUserString
title: IMetaDataTables::GetNextUserString (rometadataapi.h)
author: windows-sdk-content
description: Gets the index of the row that contains the next hard-coded string in the current table column.
old-location: winrt\imetadatatables_getnextuserstring.htm
tech.root: WinRT
ms.assetid: d35a6622-df0a-4949-bc22-9bbd583337d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNextUserString, GetNextUserString method [Windows Runtime], GetNextUserString method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetNextUserString method, IMetaDataTables.GetNextUserString, IMetaDataTables::GetNextUserString, rometadataapi/IMetaDataTables::GetNextUserString, winrt.imetadatatables_getnextuserstring
ms.topic: method
f1_keywords: ["rometadataapi/IMetaDataTables.GetNextUserString"]
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
 - IMetaDataTables.GetNextUserString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataTables::GetNextUserString


## -description


Gets the index of the row that contains the next hard-coded string in the current table column.


## -parameters




### -param ixUserString [in]

An index value from the current string column.


### -param pNext [out]

A pointer to the row index of the next string in the column.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We do not recommend the use of this method, because it does not return consistent results. For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics". The documentation is available online; see <a href="http://go.microsoft.com/fwlink/p/?linkid=199862">ECMA C# and Common Language Infrastructure Standards</a> on MSDN and <a href="http://go.microsoft.com/fwlink/p/?linkid=65552">Standard ECMA-335 - Common Language Infrastructure (CLI)</a> on the Ecma International Web site.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>
 

 

