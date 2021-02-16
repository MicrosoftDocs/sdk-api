---
UID: NF:sbtsv.ITsSbGlobalStore.QueryTarget
title: ITsSbGlobalStore::QueryTarget (sbtsv.h)
description: Retrieves the ITsSbTarget object for the given parameters.
helpviewer_keywords: ["ITsSbGlobalStore interface [Remote Desktop Services]","QueryTarget method","ITsSbGlobalStore.QueryTarget","ITsSbGlobalStore::QueryTarget","QueryTarget","QueryTarget method [Remote Desktop Services]","QueryTarget method [Remote Desktop Services]","ITsSbGlobalStore interface","sbtsv/ITsSbGlobalStore::QueryTarget","termserv.itssbglobalstore_querytarget"]
old-location: termserv\itssbglobalstore_querytarget.htm
tech.root: TermServ
ms.assetid: e89ed692-66e5-49ed-b5d9-69eefeeae66f
ms.date: 12/05/2018
ms.keywords: ITsSbGlobalStore interface [Remote Desktop Services],QueryTarget method, ITsSbGlobalStore.QueryTarget, ITsSbGlobalStore::QueryTarget, QueryTarget, QueryTarget method [Remote Desktop Services], QueryTarget method [Remote Desktop Services],ITsSbGlobalStore interface, sbtsv/ITsSbGlobalStore::QueryTarget, termserv.itssbglobalstore_querytarget
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbGlobalStore::QueryTarget
 - sbtsv/ITsSbGlobalStore::QueryTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbGlobalStore.QueryTarget
---

# ITsSbGlobalStore::QueryTarget


## -description

Retrieves the <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> object for the given parameters.

## -parameters

### -param ProviderName [in]

The name of the resource plug-in provider.

### -param TargetName [in]

The target name.

### -param FarmName [in]

The farm name to which the target belongs. If <b>NULL</b>, the first target found is returned.

### -param ppTarget [out]

A pointer to a pointer to a target <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> object. When you have finished using the object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.

## -remarks

Any changes made to the target object returned by this method do not affect the target object stored 
in Remote Desktop Connection Broker (RD Connection Broker). The target object returned is a copy of the target object in RD Connection Broker.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore">ITsSbGlobalStore</a>