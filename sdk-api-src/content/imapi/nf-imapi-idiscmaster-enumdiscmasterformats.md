---
UID: NF:imapi.IDiscMaster.EnumDiscMasterFormats
title: IDiscMaster::EnumDiscMasterFormats (imapi.h)
description: Retrieves an enumerator for all disc mastering formats supported by this disc master object. A disc master format specifies the structure of the content in a staged image file (data/audio) and the interface that manages the staged image.
helpviewer_keywords: ["EnumDiscMasterFormats","EnumDiscMasterFormats method [IMAPI]","EnumDiscMasterFormats method [IMAPI]","IDiscMaster interface","IDiscMaster interface [IMAPI]","EnumDiscMasterFormats method","IDiscMaster.EnumDiscMasterFormats","IDiscMaster::EnumDiscMasterFormats","_win32_idiscmaster_enumdiscmasterformats","base.idiscmaster_enumdiscmasterformats","imapi.idiscmaster_enumdiscmasterformats","imapi/IDiscMaster::EnumDiscMasterFormats"]
old-location: imapi\idiscmaster_enumdiscmasterformats.htm
tech.root: imapi
ms.assetid: 7190dbf6-6458-4228-a892-428183ea2742
ms.date: 12/05/2018
ms.keywords: EnumDiscMasterFormats, EnumDiscMasterFormats method [IMAPI], EnumDiscMasterFormats method [IMAPI],IDiscMaster interface, IDiscMaster interface [IMAPI],EnumDiscMasterFormats method, IDiscMaster.EnumDiscMasterFormats, IDiscMaster::EnumDiscMasterFormats, _win32_idiscmaster_enumdiscmasterformats, base.idiscmaster_enumdiscmasterformats, imapi.idiscmaster_enumdiscmasterformats, imapi/IDiscMaster::EnumDiscMasterFormats
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
 - IDiscMaster::EnumDiscMasterFormats
 - imapi/IDiscMaster::EnumDiscMasterFormats
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
 - IDiscMaster.EnumDiscMasterFormats
---

# IDiscMaster::EnumDiscMasterFormats


## -description

Retrieves an enumerator for all disc mastering formats supported by this disc master object. A disc master format specifies the structure of the content in a staged image file (data/audio) and the interface that manages the staged image.

## -parameters

### -param ppEnum [out]

Address of a pointer to the <b>IEnumDiscMasterFormats</b> enumerator.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

<b>MSDiscMasterObj</b> returns an enumerator that identifies the supported formats by their interface IDs. Currently, there are two formats: IID_IRedbookDiscMaster (
<a href="/windows/desktop/api/imapi/nn-imapi-iredbookdiscmaster">IRedbookDiscMaster</a>) and IID_IJolietDiscMaster (
<a href="/windows/desktop/api/imapi/nn-imapi-ijolietdiscmaster">IJolietDiscMaster</a>).

<b>IEnumDiscMasterFormats</b> is standard COM enumerator, as documented in 
<b>IEnumXXXX</b>. Each call to <b>Next</b> returns an array of IIDs, one IID per supported disc master format. To select the active format and retrieve a pointer to a format specific interface, use 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscmasterformat">SetActiveDiscMasterFormat</a>. (Do not use <b>QueryInterface</b>, because the interface will not be associated with the active format).

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>