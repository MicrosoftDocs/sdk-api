---
UID: NF:azroles.IAzBizRuleInterfaces.AddInterface
title: IAzBizRuleInterfaces::AddInterface (azroles.h)
description: Adds the specified interface to the list of IDispatch interfaces that can be called by business rule (BizRule) scripts.
helpviewer_keywords: ["AddInterface","AddInterface method [Security]","AddInterface method [Security]","IAzBizRuleInterfaces interface","IAzBizRuleInterfaces interface [Security]","AddInterface method","IAzBizRuleInterfaces.AddInterface","IAzBizRuleInterfaces::AddInterface","azroles/IAzBizRuleInterfaces::AddInterface","security.iazbizruleinterfaces_addinterface"]
old-location: security\iazbizruleinterfaces_addinterface.htm
tech.root: security
ms.assetid: 063492b9-9970-4605-84f5-d8b80afc719b
ms.date: 12/05/2018
ms.keywords: AddInterface, AddInterface method [Security], AddInterface method [Security],IAzBizRuleInterfaces interface, IAzBizRuleInterfaces interface [Security],AddInterface method, IAzBizRuleInterfaces.AddInterface, IAzBizRuleInterfaces::AddInterface, azroles/IAzBizRuleInterfaces::AddInterface, security.iazbizruleinterfaces_addinterface
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
 - IAzBizRuleInterfaces::AddInterface
 - azroles/IAzBizRuleInterfaces::AddInterface
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
 - IAzBizRuleInterfaces.AddInterface
---

# IAzBizRuleInterfaces::AddInterface


## -description

The <b>AddInterface</b> method adds the specified interface to the list of <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interfaces that can be called by business rule (BizRule) scripts. To add the specified interface, AzMan calls the  <a href="/scripting/winscript/reference/iactivescript-addnameditem">AddNamedItem</a> method of the <a href="/scripting/winscript/reference/iactivescript">IActiveScript</a> interface.

## -parameters

### -param bstrInterfaceName [in]

A string that contains the name used by scripts to call the interface specified by the <i>varInterface</i> parameter.

### -param lInterfaceFlag [in]

Flags sent to the <a href="/scripting/winscript/reference/iactivescript-addnameditem">AddNamedItem</a> method of the <a href="/scripting/winscript/reference/iactivescript">IActiveScript</a> interface. The <b>AddNamedItem</b> always behaves as if the <b>SCRIPTITEM_ISVISIBLE</b> flag is set, and the <b>SCRIPTITEM_ISPERSISTENT</b> flag is not set.

### -param varInterface [in]

The ID of the interface to be added.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/azroles/nn-azroles-iazbizruleinterfaces">IAzBizRuleInterfaces</a>