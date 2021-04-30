---
UID: NF:imapi.IJolietDiscMaster.SetJolietProperties
title: IJolietDiscMaster::SetJolietProperties (imapi.h)
description: Sets the Joliet properties.
helpviewer_keywords: ["IJolietDiscMaster interface [IMAPI]","SetJolietProperties method","IJolietDiscMaster.SetJolietProperties","IJolietDiscMaster::SetJolietProperties","SetJolietProperties","SetJolietProperties method [IMAPI]","SetJolietProperties method [IMAPI]","IJolietDiscMaster interface","_win32_ijolietdiscmaster_setjolietproperties","base.ijolietdiscmaster_setjolietproperties","imapi.ijolietdiscmaster_setjolietproperties","imapi/IJolietDiscMaster::SetJolietProperties"]
old-location: imapi\ijolietdiscmaster_setjolietproperties.htm
tech.root: imapi
ms.assetid: 467f8fb8-2a82-46d2-b304-3c3a600a9c63
ms.date: 12/05/2018
ms.keywords: IJolietDiscMaster interface [IMAPI],SetJolietProperties method, IJolietDiscMaster.SetJolietProperties, IJolietDiscMaster::SetJolietProperties, SetJolietProperties, SetJolietProperties method [IMAPI], SetJolietProperties method [IMAPI],IJolietDiscMaster interface, _win32_ijolietdiscmaster_setjolietproperties, base.ijolietdiscmaster_setjolietproperties, imapi.ijolietdiscmaster_setjolietproperties, imapi/IJolietDiscMaster::SetJolietProperties
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
 - IJolietDiscMaster::SetJolietProperties
 - imapi/IJolietDiscMaster::SetJolietProperties
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
 - IJolietDiscMaster.SetJolietProperties
---

# IJolietDiscMaster::SetJolietProperties


## -description

Sets the Joliet properties.

## -parameters

### -param pPropStg [in]

Pointer to the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface that the Joliet interface can use to retrieve new settings on various properties.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

Applications should query for a property set using 
<a href="/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-getjolietproperties">GetJolietProperties</a>, modify only those settings of interest, and then call 
<b>SetJolietProperties</b> to change all values simultaneously.

Some properties are read-only. Both read-only properties and unsupported properties are ignored without generating an error (see IMAPI_S_PROPERTIESIGNORED). For example, someone could submit a property set to this interface and attempt to change the ClearlyNeverHeardOfBefore property. Because ClearlyNeverHeardOfBefore is an unknown value, the property is ignored and the method succeeds.

After calling 
<b>SetJolietProperties</b>, an application should verify property settings by calling 
<a href="/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-getjolietproperties">GetJolietProperties</a>.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-ijolietdiscmaster">IJolietDiscMaster</a>