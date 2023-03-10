---
UID: NF:pla.ITraceDataProvider.GetSecurity
title: ITraceDataProvider::GetSecurity (pla.h)
description: Retrieves the security information for the trace data provider.
helpviewer_keywords: ["GetSecurity","GetSecurity method [PLA]","GetSecurity method [PLA]","ITraceDataProvider interface","ITraceDataProvider interface [PLA]","GetSecurity method","ITraceDataProvider.GetSecurity","ITraceDataProvider::GetSecurity","pla.itracedataprovider_getsecurity","pla/ITraceDataProvider::GetSecurity"]
old-location: pla\itracedataprovider_getsecurity.htm
tech.root: PLA
ms.assetid: 2f1618db-aa43-4cac-a652-db172781e988
ms.date: 12/05/2018
ms.keywords: GetSecurity, GetSecurity method [PLA], GetSecurity method [PLA],ITraceDataProvider interface, ITraceDataProvider interface [PLA],GetSecurity method, ITraceDataProvider.GetSecurity, ITraceDataProvider::GetSecurity, pla.itracedataprovider_getsecurity, pla/ITraceDataProvider::GetSecurity
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITraceDataProvider::GetSecurity
 - pla/ITraceDataProvider::GetSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ITraceDataProvider.GetSecurity
---

# ITraceDataProvider::GetSecurity


## -description

Retrieves the security information for the trace data provider.

## -parameters

### -param SecurityInfo [in]

The object-related security information. For details, see the <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> data type.

### -param Sddl [out]

A string that describes the security descriptor for the object. For details, see <a href="/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor Definition Language</a>.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-setsecurity">ITraceDataProvider::SetSecurity</a>