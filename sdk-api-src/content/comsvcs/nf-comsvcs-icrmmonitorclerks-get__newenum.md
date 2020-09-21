---
UID: NF:comsvcs.ICrmMonitorClerks.get__NewEnum
title: ICrmMonitorClerks::get__NewEnum (comsvcs.h)
description: Retrieves an enumerator for the instance CLSIDs of the CRM clerks.
helpviewer_keywords: ["ICrmMonitorClerks interface [COM+]","get__NewEnum method","ICrmMonitorClerks.get__NewEnum","ICrmMonitorClerks::get__NewEnum","_dtc_ICrmMonitorClerks__NewEnum","comsvcs/ICrmMonitorClerks::get__NewEnum","cos.icrmmonitorclerks_get__newenum","get__NewEnum","get__NewEnum method [COM+]","get__NewEnum method [COM+]","ICrmMonitorClerks interface"]
old-location: cos\icrmmonitorclerks_get__newenum.htm
tech.root: cos
ms.assetid: bbebfa75-7ca1-46fb-b246-7f3c312987fa
ms.date: 12/05/2018
ms.keywords: ICrmMonitorClerks interface [COM+],get__NewEnum method, ICrmMonitorClerks.get__NewEnum, ICrmMonitorClerks::get__NewEnum, _dtc_ICrmMonitorClerks__NewEnum, comsvcs/ICrmMonitorClerks::get__NewEnum, cos.icrmmonitorclerks_get__newenum, get__NewEnum, get__NewEnum method [COM+], get__NewEnum method [COM+],ICrmMonitorClerks interface
req.header: comsvcs.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICrmMonitorClerks::get__NewEnum
 - comsvcs/ICrmMonitorClerks::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmMonitorClerks.get__NewEnum
---

# ICrmMonitorClerks::get__NewEnum


## -description

Retrieves an enumerator for the instance CLSIDs of the CRM clerks.

## -parameters

### -param pVal [out]

A reference to the returned <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitorclerks">ICrmMonitorClerks</a>