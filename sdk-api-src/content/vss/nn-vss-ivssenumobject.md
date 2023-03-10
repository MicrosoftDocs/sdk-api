---
UID: NN:vss.IVssEnumObject
title: IVssEnumObject (vss.h)
description: Contains methods to iterate over and perform other operations on a list of enumerated objects. (IVssEnumObject)
helpviewer_keywords: ["IVssEnumObject","IVssEnumObject interface [VSS]","IVssEnumObject interface [VSS]","described","_win32_ivssenumobject","base.ivssenumobject","vss/IVssEnumObject"]
old-location: base\ivssenumobject.htm
tech.root: base
ms.assetid: b8e80909-a28a-45d7-87e2-4f44bf6990f4
ms.date: 12/05/2018
ms.keywords: IVssEnumObject, IVssEnumObject interface [VSS], IVssEnumObject interface [VSS],described, _win32_ivssenumobject, base.ivssenumobject, vss/IVssEnumObject
req.header: vss.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssEnumObject
 - vss/IVssEnumObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssEnumObject
---

# IVssEnumObject interface


## -description

The <b>IVssEnumObject</b> interface contains methods 
    to iterate over and perform other operations on a list of enumerated objects.

The calling application is responsible for calling 
    <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the resources held by the 
    returned <b>IVssEnumObject</b> when it is no longer needed. It 
    may also need to call <b>IUnknown::Release</b> to release 
    temporary objects (such as strings) returned during enumeration.

The <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">IVssBackupComponents::Query</a> method 
    returns an <b>IVssEnumObject</b> object.

## -inheritance

The <b>IVssEnumObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssEnumObject</b> also has these types of members:

