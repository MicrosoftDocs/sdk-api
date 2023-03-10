---
UID: NF:imapi.IDiscMaster.GetActiveDiscMasterFormat
title: IDiscMaster::GetActiveDiscMasterFormat (imapi.h)
description: Retrieves the active disc recorder format. The active format specifies both the structure of the staged image file content (audio/data) and the COM interface that must be used to manipulate that staged image.
helpviewer_keywords: ["GetActiveDiscMasterFormat","GetActiveDiscMasterFormat method [IMAPI]","GetActiveDiscMasterFormat method [IMAPI]","IDiscMaster interface","IDiscMaster interface [IMAPI]","GetActiveDiscMasterFormat method","IDiscMaster.GetActiveDiscMasterFormat","IDiscMaster::GetActiveDiscMasterFormat","_win32_idiscmaster_getactivediscmasterformat","base.idiscmaster_getactivediscmasterformat","imapi.idiscmaster_getactivediscmasterformat","imapi/IDiscMaster::GetActiveDiscMasterFormat"]
old-location: imapi\idiscmaster_getactivediscmasterformat.htm
tech.root: imapi
ms.assetid: 37677090-fa1d-4515-9b01-13bfa55d8ebb
ms.date: 12/05/2018
ms.keywords: GetActiveDiscMasterFormat, GetActiveDiscMasterFormat method [IMAPI], GetActiveDiscMasterFormat method [IMAPI],IDiscMaster interface, IDiscMaster interface [IMAPI],GetActiveDiscMasterFormat method, IDiscMaster.GetActiveDiscMasterFormat, IDiscMaster::GetActiveDiscMasterFormat, _win32_idiscmaster_getactivediscmasterformat, base.idiscmaster_getactivediscmasterformat, imapi.idiscmaster_getactivediscmasterformat, imapi/IDiscMaster::GetActiveDiscMasterFormat
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscMaster::GetActiveDiscMasterFormat
 - imapi/IDiscMaster::GetActiveDiscMasterFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscMaster.GetActiveDiscMasterFormat
---

# IDiscMaster::GetActiveDiscMasterFormat


## -description

Retrieves the active disc recorder format. The active format specifies both the structure of the staged image file content (audio/data) and the COM interface that must be used to manipulate that staged image.

## -parameters

### -param lpiid [out]

IID of the currently active format.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

<b>MSDiscMasterObj</b> supports the IIDs for two formats: IID_IRedbookDiscMaster (<a href="/windows/desktop/api/imapi/nn-imapi-iredbookdiscmaster">IRedbookDiscMaster</a>) and IID_IJolietDiscMaster (<a href="/windows/desktop/api/imapi/nn-imapi-ijolietdiscmaster">IJolietDiscMaster</a>). To select the active format and retrieve a pointer to a format-specific interface, use 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscmasterformat">SetActiveDiscMasterFormat</a>.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>