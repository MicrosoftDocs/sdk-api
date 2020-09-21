---
UID: NF:sbtsv.ITsSbProvider.CreateLoadBalanceResultObject
title: ITsSbProvider::CreateLoadBalanceResultObject (sbtsv.h)
description: Creates an ITsSbLoadBalanceResult load-balancing result object.
helpviewer_keywords: ["CreateLoadBalanceResultObject","CreateLoadBalanceResultObject method [Remote Desktop Services]","CreateLoadBalanceResultObject method [Remote Desktop Services]","ITsSbProvider interface","ITsSbProvider interface [Remote Desktop Services]","CreateLoadBalanceResultObject method","ITsSbProvider.CreateLoadBalanceResultObject","ITsSbProvider::CreateLoadBalanceResultObject","sbtsv/ITsSbProvider::CreateLoadBalanceResultObject","termserv.itssbprovider_createloadbalanceresultobject"]
old-location: termserv\itssbprovider_createloadbalanceresultobject.htm
tech.root: TermServ
ms.assetid: aaa13ec1-d79c-4458-9340-3cc42bbcd948
ms.date: 12/05/2018
ms.keywords: CreateLoadBalanceResultObject, CreateLoadBalanceResultObject method [Remote Desktop Services], CreateLoadBalanceResultObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateLoadBalanceResultObject method, ITsSbProvider.CreateLoadBalanceResultObject, ITsSbProvider::CreateLoadBalanceResultObject, sbtsv/ITsSbProvider::CreateLoadBalanceResultObject, termserv.itssbprovider_createloadbalanceresultobject
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
 - ITsSbProvider::CreateLoadBalanceResultObject
 - sbtsv/ITsSbProvider::CreateLoadBalanceResultObject
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
 - ITsSbProvider.CreateLoadBalanceResultObject
---

# ITsSbProvider::CreateLoadBalanceResultObject


## -description

Creates an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a> load-balancing result 
object.

## -parameters

### -param TargetName [in]

A <b>BSTR</b> variable that contains the target name.

### -param ppLBResult [out]

A pointer to a pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a> object. When you have finished using the object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

## -returns

This method can return one of these values.


If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.

## -remarks

Plug-ins can use this method to create a load-balancing result 
object.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>