---
UID: NF:iads.IADsADSystemInfo.GetAnyDCName
title: IADsADSystemInfo::GetAnyDCName (iads.h)
description: Retrieves the DNS name of a domain controller in the local computer's domain.
helpviewer_keywords: ["GetAnyDCName","GetAnyDCName method [ADSI]","GetAnyDCName method [ADSI]","IADsADSystemInfo interface","IADsADSystemInfo interface [ADSI]","GetAnyDCName method","IADsADSystemInfo.GetAnyDCName","IADsADSystemInfo::GetAnyDCName","_ds_iadsadsysteminfo_getanydcname","adsi.iadsadsysteminfo__getanydcname","adsi.iadsadsysteminfo_getanydcname","iads/IADsADSystemInfo::GetAnyDCName"]
old-location: adsi\iadsadsysteminfo_getanydcname.htm
tech.root: adsi
ms.assetid: 02bc092a-f5ef-4f9d-b9a6-e03aba784d66
ms.date: 12/05/2018
ms.keywords: GetAnyDCName, GetAnyDCName method [ADSI], GetAnyDCName method [ADSI],IADsADSystemInfo interface, IADsADSystemInfo interface [ADSI],GetAnyDCName method, IADsADSystemInfo.GetAnyDCName, IADsADSystemInfo::GetAnyDCName, _ds_iadsadsysteminfo_getanydcname, adsi.iadsadsysteminfo__getanydcname, adsi.iadsadsysteminfo_getanydcname, iads/IADsADSystemInfo::GetAnyDCName
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
 - IADsADSystemInfo::GetAnyDCName
 - iads/IADsADSystemInfo::GetAnyDCName
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
 - IADsADSystemInfo.GetAnyDCName
---

# IADsADSystemInfo::GetAnyDCName


## -description

The <b>IADsADSystemInfo::GetAnyDCName</b> method retrieves the DNS name of a domain controller in the local computer's domain.

## -parameters

### -param pszDCName [out]

Name of a domain controller, such as "ADServer1.domain1.Fabrikam.com".

## -returns

This method supports the standard <b>HRESULT</b> return values. For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsadsysteminfo">IADsADSystemInfo</a>