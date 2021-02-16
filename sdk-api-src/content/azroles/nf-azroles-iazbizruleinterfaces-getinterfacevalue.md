---
UID: NF:azroles.IAzBizRuleInterfaces.GetInterfaceValue
title: IAzBizRuleInterfaces::GetInterfaceValue (azroles.h)
description: Gets the ID and flags of the interface that corresponds to the specified interface name.
helpviewer_keywords: ["GetInterfaceValue","GetInterfaceValue method [Security]","GetInterfaceValue method [Security]","IAzBizRuleInterfaces interface","IAzBizRuleInterfaces interface [Security]","GetInterfaceValue method","IAzBizRuleInterfaces.GetInterfaceValue","IAzBizRuleInterfaces::GetInterfaceValue","azroles/IAzBizRuleInterfaces::GetInterfaceValue","security.iazbizruleinterfaces_getinterfacevalue_method"]
old-location: security\iazbizruleinterfaces_getinterfacevalue_method.htm
tech.root: security
ms.assetid: d5d12529-6ce8-4189-949b-210d8ec84084
ms.date: 12/05/2018
ms.keywords: GetInterfaceValue, GetInterfaceValue method [Security], GetInterfaceValue method [Security],IAzBizRuleInterfaces interface, IAzBizRuleInterfaces interface [Security],GetInterfaceValue method, IAzBizRuleInterfaces.GetInterfaceValue, IAzBizRuleInterfaces::GetInterfaceValue, azroles/IAzBizRuleInterfaces::GetInterfaceValue, security.iazbizruleinterfaces_getinterfacevalue_method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
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
 - IAzBizRuleInterfaces::GetInterfaceValue
 - azroles/IAzBizRuleInterfaces::GetInterfaceValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzBizRuleInterfaces.GetInterfaceValue
---

# IAzBizRuleInterfaces::GetInterfaceValue


## -description

The <b>GetInterfaceValue</b> method gets the ID and flags of the interface that corresponds to the specified interface name.

## -parameters

### -param bstrInterfaceName [in]

A string that contains the interface name.

### -param lInterfaceFlag [out]

A pointer to the flags associated with the interface name.

### -param varInterface [out]

A pointer to the ID associated with the interface name.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/azroles/nf-azroles-iazbizruleinterfaces-addinterface">AddInterface</a>



<a href="/windows/desktop/api/azroles/nn-azroles-iazbizruleinterfaces">IAzBizRuleInterfaces</a>