---
UID: NF:azroles.IAzBizRuleInterfaces.Remove
title: IAzBizRuleInterfaces::Remove (azroles.h)
description: Removes the specified interface from the list of interfaces The number of interfaces in the list of interfaces that can be called by BizRule scripts.
helpviewer_keywords: ["IAzBizRuleInterfaces interface [Security]","Remove method","IAzBizRuleInterfaces.Remove","IAzBizRuleInterfaces::Remove","Remove","Remove method [Security]","Remove method [Security]","IAzBizRuleInterfaces interface","azroles/IAzBizRuleInterfaces::Remove","security.iazbizruleinterfaces_remove_method"]
old-location: security\iazbizruleinterfaces_remove_method.htm
tech.root: SecAuthZ
ms.assetid: 398e4151-aeda-48d0-b6f5-e0ea749d0720
ms.date: 12/05/2018
ms.keywords: IAzBizRuleInterfaces interface [Security],Remove method, IAzBizRuleInterfaces.Remove, IAzBizRuleInterfaces::Remove, Remove, Remove method [Security], Remove method [Security],IAzBizRuleInterfaces interface, azroles/IAzBizRuleInterfaces::Remove, security.iazbizruleinterfaces_remove_method
f1_keywords:
- azroles/IAzBizRuleInterfaces.Remove
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.h
api_name:
- IAzBizRuleInterfaces.Remove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzBizRuleInterfaces::Remove


## -description


The <b>Remove</b> method removes the specified interface from the list of interfaces The number of interfaces in the list of interfaces that can be called by BizRule scripts.


## -parameters




### -param bstrInterfaceName [in]

The name of the interface to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizruleinterfaces-addinterface">AddInterface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazbizruleinterfaces">IAzBizRuleInterfaces</a>
 

 

