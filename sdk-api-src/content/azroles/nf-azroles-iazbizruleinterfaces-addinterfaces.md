---
UID: NF:azroles.IAzBizRuleInterfaces.AddInterfaces
title: IAzBizRuleInterfaces::AddInterfaces (azroles.h)
description: Adds the specified interfaces to the list of IDispatch interfaces that can be called by business rule (BizRule) scripts.
helpviewer_keywords: ["AddInterfaces","AddInterfaces method [Security]","AddInterfaces method [Security]","IAzBizRuleInterfaces interface","IAzBizRuleInterfaces interface [Security]","AddInterfaces method","IAzBizRuleInterfaces.AddInterfaces","IAzBizRuleInterfaces::AddInterfaces","azroles/IAzBizRuleInterfaces::AddInterfaces","security.iazbizruleinterfaces_addinterfaces_method"]
old-location: security\iazbizruleinterfaces_addinterfaces_method.htm
tech.root: security
ms.assetid: 91822c84-4daa-4d3c-bbe2-9ceb7fc642b2
ms.date: 12/05/2018
ms.keywords: AddInterfaces, AddInterfaces method [Security], AddInterfaces method [Security],IAzBizRuleInterfaces interface, IAzBizRuleInterfaces interface [Security],AddInterfaces method, IAzBizRuleInterfaces.AddInterfaces, IAzBizRuleInterfaces::AddInterfaces, azroles/IAzBizRuleInterfaces::AddInterfaces, security.iazbizruleinterfaces_addinterfaces_method
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
 - IAzBizRuleInterfaces::AddInterfaces
 - azroles/IAzBizRuleInterfaces::AddInterfaces
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
 - IAzBizRuleInterfaces.AddInterfaces
---

# IAzBizRuleInterfaces::AddInterfaces


## -description

The <b>AddInterfaces</b> method adds the specified interfaces to the list of <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interfaces that can be called by business rule (BizRule) scripts. To add the specified interfaces, AzMan calls the <a href="/scripting/winscript/reference/iactivescript-addnameditem">AddNamedItem</a> method of the <a href="/scripting/winscript/reference/iactivescript">IActiveScript</a> interface once for each specified interface.

## -parameters

### -param varInterfaceNames [in]

A <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that specifies the names that scripts use to call the interfaces specified by the <i>varInterfaces</i> array.

### -param varInterfaceFlags [in]

A <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that specifies flags sent to the <a href="/scripting/winscript/reference/iactivescript-addnameditem">AddNamedItem</a> method of the <a href="/scripting/winscript/reference/iactivescript">IActiveScript</a> interface. The <b>AddNamedItem</b> always behaves as if the <b>SCRIPTITEM_ISVISIBLE</b> flag is set, and the <b>SCRIPTITEM_ISPERSISTENT</b> flag is not set.

### -param varInterfaces [in]

A <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that specifies the IDs of the interfaces to be added.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The names of the interfaces specified by the <i>varInterfaceNames</i> array are in the same order as the corresponding interface IDs specified by the <i>varInterfaces</i> array.