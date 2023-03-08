---
UID: NF:iads.IADsADSystemInfo.RefreshSchemaCache
title: IADsADSystemInfo::RefreshSchemaCache (iads.h)
description: The IADsADSystemInfo::RefreshSchemaCache method refreshes the Active Directory schema cache.
helpviewer_keywords: ["IADsADSystemInfo interface [ADSI]","RefreshSchemaCache method","IADsADSystemInfo.RefreshSchemaCache","IADsADSystemInfo::RefreshSchemaCache","RefreshSchemaCache","RefreshSchemaCache method [ADSI]","RefreshSchemaCache method [ADSI]","IADsADSystemInfo interface","_ds_iadsadsysteminfo_refreshschemacache","adsi.iadsadsysteminfo__refreshschemacache","adsi.iadsadsysteminfo_refreshschemacache","iads/IADsADSystemInfo::RefreshSchemaCache"]
old-location: adsi\iadsadsysteminfo_refreshschemacache.htm
tech.root: adsi
ms.assetid: 4531c041-a5a7-4de1-a3c4-c544cb4d6820
ms.date: 12/05/2018
ms.keywords: IADsADSystemInfo interface [ADSI],RefreshSchemaCache method, IADsADSystemInfo.RefreshSchemaCache, IADsADSystemInfo::RefreshSchemaCache, RefreshSchemaCache, RefreshSchemaCache method [ADSI], RefreshSchemaCache method [ADSI],IADsADSystemInfo interface, _ds_iadsadsysteminfo_refreshschemacache, adsi.iadsadsysteminfo__refreshschemacache, adsi.iadsadsysteminfo_refreshschemacache, iads/IADsADSystemInfo::RefreshSchemaCache
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
 - IADsADSystemInfo::RefreshSchemaCache
 - iads/IADsADSystemInfo::RefreshSchemaCache
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
 - IADsADSystemInfo.RefreshSchemaCache
---

# IADsADSystemInfo::RefreshSchemaCache


## -description

The <b>IADsADSystemInfo::RefreshSchemaCache</b> method refreshes the Active Directory schema cache.



## -returns

This method supports the standard <b>HRESULT</b> return values. For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

When you call this method, it does a Put() of the <b>schemaUpdateNow</b> function on the RootDSE. Normally, when you make changes to the schema, they are not updated to the RootDSE until the next automatic update. This method does an immediate update to the schema so that you can view the changes to the schema.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsadsysteminfo">IADsADSystemInfo</a>
