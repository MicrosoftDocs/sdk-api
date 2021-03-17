---
UID: NF:cscobj.IOfflineFilesSetting.GetName
title: IOfflineFilesSetting::GetName (cscobj.h)
description: Retrieves a name associated with a particular Offline Files setting.
helpviewer_keywords: ["GetName","GetName method [Offline Files]","GetName method [Offline Files]","IOfflineFilesSetting interface","IOfflineFilesSetting interface [Offline Files]","GetName method","IOfflineFilesSetting.GetName","IOfflineFilesSetting::GetName","cscobj/IOfflineFilesSetting::GetName","of.iofflinefilessetting_getname"]
old-location: of\iofflinefilessetting_getname.htm
tech.root: of
ms.assetid: 2e4591b5-c8a9-4645-8001-8ac09c706ee2
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Offline Files], GetName method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],GetName method, IOfflineFilesSetting.GetName, IOfflineFilesSetting::GetName, cscobj/IOfflineFilesSetting::GetName, of.iofflinefilessetting_getname
req.header: cscobj.h
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesSetting::GetName
 - cscobj/IOfflineFilesSetting::GetName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSetting.GetName
---

# IOfflineFilesSetting::GetName


## -description

Retrieves a name associated with a particular Offline Files setting.

## -parameters

### -param ppszName [out]

Address of pointer variable that receives the address of a string containing the name of the Offline Files setting.  Upon successful return, the caller must free this memory block by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessetting">IOfflineFilesSetting</a>