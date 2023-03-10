---
UID: NF:azroles.IAzClientContext.AccessCheck
title: IAzClientContext::AccessCheck (azroles.h)
description: Determines whether the current client context is allowed to perform the specified operations.
helpviewer_keywords: ["AccessCheck","AccessCheck method [Security]","AccessCheck method [Security]","AzClientContext object","AccessCheck method [Security]","IAzClientContext interface","AzClientContext object [Security]","AccessCheck method","IAzClientContext interface [Security]","AccessCheck method","IAzClientContext.AccessCheck","IAzClientContext::AccessCheck","azroles/IAzClientContext::AccessCheck","security.iazclientcontext_accesscheck"]
old-location: security\iazclientcontext_accesscheck.htm
tech.root: security
ms.assetid: 0bd16cdb-3dba-4656-b264-32e622732155
ms.date: 12/05/2018
ms.keywords: AccessCheck, AccessCheck method [Security], AccessCheck method [Security],AzClientContext object, AccessCheck method [Security],IAzClientContext interface, AzClientContext object [Security],AccessCheck method, IAzClientContext interface [Security],AccessCheck method, IAzClientContext.AccessCheck, IAzClientContext::AccessCheck, azroles/IAzClientContext::AccessCheck, security.iazclientcontext_accesscheck
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzClientContext::AccessCheck
 - azroles/IAzClientContext::AccessCheck
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext.AccessCheck
 - AzClientContext.AccessCheck
---

# IAzClientContext::AccessCheck


## -description

The <b>AccessCheck</b> method determines whether the current client context is allowed to perform the specified operations.

## -parameters

### -param bstrObjectName [in]

The name of the accessed object. This string is used in audits.

### -param varScopeNames [in]

A variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds  a <b>VT_BSTR</b> that contains the name of a scope that the object specified by the <i>bstrObjectName</i> parameter matches. The array can contain only one element. To use the default application level scope, set the first entry in the array to an empty string ("") or <b>VT_EMPTY</b>, or pass <b>VT_EMPTY</b> in to this parameter.

### -param varOperations [in]

The operations for which access by the client context is checked. This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the  JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_I2</b> or <b>VT_I4</b> that represents the <a href="/windows/desktop/api/azroles/nf-azroles-iazoperation-get_operationid">OperationID</a> property of an <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object in the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> policy.

### -param varParameterNames [in, optional]

The names of the parameters available to business rules (BizRules) through the <a href="/windows/desktop/api/azroles/nf-azroles-iazbizrulecontext-getparameter">AzBizRuleContext::GetParameter</a> method. This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the  JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a parameter name. This array must be sorted alphabetically by the caller; the sort order is as defined by a case-sensitive <a href="/windows/desktop/api/oleauto/nf-oleauto-varcmp">VarCmp</a>. The order of the <i>varParameterValues</i> array must match the order of this array. The default value is <b>VT_NULL</b>.

### -param varParameterValues [in, optional]

The values of the parameters that are available to business rules (BizRules) through the <a href="/windows/desktop/api/azroles/nf-azroles-iazbizrulecontext-getparameter">AzBizRuleContext::GetParameter</a> method. This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the  JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a value that corresponds to an element in the <i>varParameterNames</i> array. The default value is <b>VT_NULL</b>. The entries in the array can hold any type except <b>VT_UNKNOWN</b> and <b>VT_DISPATCH</b>.

### -param varInterfaceNames [in, optional]

The names by which the interfaces in the <i>varInterfaces</i> array will be known in a BizRule script. This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the  JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a string variant that contains an interface name. This method calls the <a href="/scripting/winscript/reference/iactivescript-addnameditem">IActiveScript::AddNamedItem</a> method for each entry in the array. The default value is <b>VT_NULL</b>.

### -param varInterfaceFlags [in, optional]

Flags that will be passed in the call to <a href="/scripting/winscript/reference/iactivescript-addnameditem">IActiveScript::AddNamedItem</a>. This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the  JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_I4</b>. The SCRIPTITEM_ISVISIBLE flag is implied; the SCRIPTITEM_ISPERSISTENT flag is ignored. Each entry in the array must match the corresponding element in the <i>varInterfaceNames</i> array. The default value is <b>VT_NULL</b>.

### -param varInterfaces [in, optional]

The <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interfaces that will be made available to the BizRule script. This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the  JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds an <b>IDispatch</b> interface. Each entry in the array must match the corresponding element in the <i>varInterfaceNames</i> array. The default value is <b>VT_NULL</b>.

### -param pvarResults [out]

A pointer to a <b>VARIANT</b> used to return a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that contains the results of the access check. Each element of the <b>SAFEARRAY</b> is a <b>VARIANT</b> of type <b>VT_I4</b>. Each entry in the array  matches the corresponding element in the <i>varOperations</i> array. If access to an operation is granted to the client context, a value of NO_ERROR is returned in the corresponding element in the <i>pvarResults</i> array. Any other value indicates that access to that operation is not granted. A typical value that indicates failure is ERROR_ACCESS_DENIED.

In  JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.

## -returns

If the method succeeds, the method returns NO_ERROR.

If the method fails, it returns an <b>HRESULT</b> value that indicates the status of the method, not the result of the access check. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_CORRUPT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
This error code can be returned if an Active Directory authorization store is used and the administration of the scope has been delegated. The task and role definitions within a delegated scope cannot have BizRules. If a task or role definition within a delegated scope contains a BizRule (this is possible if the store is corrupted), the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method will fail.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLESCRIPT_E_SYNTAX</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The BizRule used to evaluate access contains a syntax error.

</td>
</tr>
</table>

## -remarks

If the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck">RoleForAccessCheck</a> property is defined in the client context, the <b>AccessCheck</b> method will be performed only on that role.

When this method is called, the application group membership is added to the client context so that it does not need to be recomputed for subsequent access checks on the same client context.

This method cannot be called by a BizRule.