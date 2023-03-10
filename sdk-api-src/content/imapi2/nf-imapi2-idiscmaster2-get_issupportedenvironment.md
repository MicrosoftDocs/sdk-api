---
UID: NF:imapi2.IDiscMaster2.get_IsSupportedEnvironment
title: IDiscMaster2::get_IsSupportedEnvironment (imapi2.h)
description: Retrieves a value that determines if the environment contains one or more optical devices and the execution context has permission to access the devices.
helpviewer_keywords: ["IDiscMaster2 interface [IMAPI]","get_IsSupportedEnvironment method","IDiscMaster2.get_IsSupportedEnvironment","IDiscMaster2::get_IsSupportedEnvironment","get_IsSupportedEnvironment","get_IsSupportedEnvironment method [IMAPI]","get_IsSupportedEnvironment method [IMAPI]","IDiscMaster2 interface","imapi.idiscmaster2_get_issupportedenvironment","imapi2/IDiscMaster2::get_IsSupportedEnvironment"]
old-location: imapi\idiscmaster2_get_issupportedenvironment.htm
tech.root: imapi
ms.assetid: abaa4d89-07b2-4e7a-a0c9-8a31abfd9dd0
ms.date: 12/05/2018
ms.keywords: IDiscMaster2 interface [IMAPI],get_IsSupportedEnvironment method, IDiscMaster2.get_IsSupportedEnvironment, IDiscMaster2::get_IsSupportedEnvironment, get_IsSupportedEnvironment, get_IsSupportedEnvironment method [IMAPI], get_IsSupportedEnvironment method [IMAPI],IDiscMaster2 interface, imapi.idiscmaster2_get_issupportedenvironment, imapi2/IDiscMaster2::get_IsSupportedEnvironment
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IDiscMaster2::get_IsSupportedEnvironment
 - imapi2/IDiscMaster2::get_IsSupportedEnvironment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscMaster2.get_IsSupportedEnvironment
---

# IDiscMaster2::get_IsSupportedEnvironment


## -description

Retrieves a value that determines if the environment contains one or more optical devices and the execution context has permission to access the devices.

## -parameters

### -param value

Is VARIANT_TRUE if the environment contains one or more optical devices and the execution context has permission to access the devices; otherwise, VARIANT_FALSE.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>

## -remarks

This method loops through all the strings in <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get_item">IDiscMaster2</a> and attempts to use each string to initialize a <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">DiscRecorder2</a> object.  If any of the recorders on the system succeed the initialization, this method returns <b>TRUE</b>.

The environment must contain at least one type-5 optical device.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2">IDiscMaster2</a>