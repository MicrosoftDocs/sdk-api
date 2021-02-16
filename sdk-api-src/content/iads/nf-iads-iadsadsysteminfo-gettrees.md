---
UID: NF:iads.IADsADSystemInfo.GetTrees
title: IADsADSystemInfo::GetTrees (iads.h)
description: Retrieves the DNS names of all the directory trees in the local computer's forest.
helpviewer_keywords: ["GetTrees","GetTrees method [ADSI]","GetTrees method [ADSI]","IADsADSystemInfo interface","IADsADSystemInfo interface [ADSI]","GetTrees method","IADsADSystemInfo.GetTrees","IADsADSystemInfo::GetTrees","_ds_iadsadsysteminfo_gettrees","adsi.iadsadsysteminfo__gettrees","adsi.iadsadsysteminfo_gettrees","iads/IADsADSystemInfo::GetTrees"]
old-location: adsi\iadsadsysteminfo_gettrees.htm
tech.root: adsi
ms.assetid: 1446d248-0adc-4542-b4af-c7139cee028f
ms.date: 12/05/2018
ms.keywords: GetTrees, GetTrees method [ADSI], GetTrees method [ADSI],IADsADSystemInfo interface, IADsADSystemInfo interface [ADSI],GetTrees method, IADsADSystemInfo.GetTrees, IADsADSystemInfo::GetTrees, _ds_iadsadsysteminfo_gettrees, adsi.iadsadsysteminfo__gettrees, adsi.iadsadsysteminfo_gettrees, iads/IADsADSystemInfo::GetTrees
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsADSystemInfo::GetTrees
 - iads/IADsADSystemInfo::GetTrees
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsADSystemInfo.GetTrees
---

# IADsADSystemInfo::GetTrees


## -description

The <b>IADsADSystemInfo::GetTrees</b> method retrieves the DNS names of all the directory trees in the local computer's forest.

## -parameters

### -param pvTrees [out]

A Variant array of strings that contains the names of the directory trees within the forest.

## -returns

This method supports the standard <b>HRESULT</b> return values. For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsadsysteminfo">IADsADSystemInfo</a>