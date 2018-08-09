---
UID: NF:azroles.IAzClientContext.AccessCheck
title: IAzClientContext::AccessCheck
author: windows-sdk-content
description: Determines whether the current client context is allowed to perform the specified operations.
old-location: security\iazclientcontext_accesscheck.htm
old-project: secauthz
ms.assetid: 0bd16cdb-3dba-4656-b264-32e622732155
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AccessCheck, AccessCheck method [Security], AccessCheck method [Security],AzClientContext object, AccessCheck method [Security],IAzClientContext interface, AzClientContext object [Security],AccessCheck method, IAzClientContext interface [Security],AccessCheck method, IAzClientContext.AccessCheck, IAzClientContext::AccessCheck, azroles/IAzClientContext::AccessCheck, security.iazclientcontext_accesscheck
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
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
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext::AccessCheck


## -description


The <b>AccessCheck</b> method determines whether the current client context is allowed to perform the specified operations.


## -parameters




### -param bstrObjectName [in]

The name of the accessed object. This string is used in audits.


### -param varScopeNames [in]

A variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds  a <b>VT_BSTR</b> that contains the name of a scope that the object specified by the <i>bstrObjectName</i> parameter matches. The array can contain only one element. To use the default application level scope, set the first entry in the array to an empty string ("") or <b>VT_EMPTY</b>, or pass <b>VT_EMPTY</b> in to this parameter.


### -param varOperations [in]

The operations for which access by the client context is checked. This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the  JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_I2</b> or <b>VT_I4</b> that represents the <a href="https://msdn.microsoft.com/3466dea1-b005-40fc-87d1-29b5e033f6a0">OperationID</a> property of an <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object in the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> policy. 


### -param varParameterNames [in, optional]

The names of the parameters available to business rules (BizRules) through the <a href="https://msdn.microsoft.com/9c956eea-92a5-4da8-abe0-a5ab4e41ab85">AzBizRuleContext::GetParameter</a> method. This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the  JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a parameter name. This array must be sorted alphabetically by the caller; the sort order is as defined by a case-sensitive <a href="00b96fa7-446c-450b-bd06-a966e1acb5ce">VarCmp</a>. The order of the <i>varParameterValues</i> array must match the order of this array. The default value is <b>VT_NULL</b>.


### -param varParameterValues [in, optional]

The values of the parameters that are available to business rules (BizRules) through the <a href="https://msdn.microsoft.com/9c956eea-92a5-4da8-abe0-a5ab4e41ab85">AzBizRuleContext::GetParameter</a> method. This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the  JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a value that corresponds to an element in the <i>varParameterNames</i> array. The default value is <b>VT_NULL</b>. The entries in the array can hold any type except <b>VT_UNKNOWN</b> and <b>VT_DISPATCH</b>.


### -param varInterfaceNames [in, optional]

The names by which the interfaces in the <i>varInterfaces</i> array will be known in a BizRule script. This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the  JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a string variant that contains an interface name. This method calls the <a href="a7c6317d-948f-4bb3-b169-1bbe5b7c7cc5">IActiveScript::AddNamedItem</a> method for each entry in the array. The default value is <b>VT_NULL</b>.


### -param varInterfaceFlags [in, optional]

Flags that will be passed in the call to <a href="a7c6317d-948f-4bb3-b169-1bbe5b7c7cc5">IActiveScript::AddNamedItem</a>. This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the  JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_I4</b>. The SCRIPTITEM_ISVISIBLE flag is implied; the SCRIPTITEM_ISPERSISTENT flag is ignored. Each entry in the array must match the corresponding element in the <i>varInterfaceNames</i> array. The default value is <b>VT_NULL</b>.


### -param varInterfaces [in, optional]

The <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interfaces that will be made available to the BizRule script. This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the  JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds an <b>IDispatch</b> interface. Each entry in the array must match the corresponding element in the <i>varInterfaceNames</i> array. The default value is <b>VT_NULL</b>.


### -param pvarResults [out]

A pointer to a <b>VARIANT</b> used to return a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> that contains the results of the access check. Each element of the <b>SAFEARRAY</b> is a <b>VARIANT</b> of type <b>VT_I4</b>. Each entry in the array  matches the corresponding element in the <i>varOperations</i> array. If access to an operation is granted to the client context, a value of NO_ERROR is returned in the corresponding element in the <i>pvarResults</i> array. Any other value indicates that access to that operation is not granted. A typical value that indicates failure is ERROR_ACCESS_DENIED.

In  JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object.


## -returns



If the method succeeds, the method returns NO_ERROR.

If the method fails, it returns an <b>HRESULT</b> value that indicates the status of the method, not the result of the access check. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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
This error code can be returned if an Active Directory authorization store is used and the administration of the scope has been delegated. The task and role definitions within a delegated scope cannot have BizRules. If a task or role definition within a delegated scope contains a BizRule (this is possible if the store is corrupted), the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method will fail.

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



If the <a href="https://msdn.microsoft.com/817b3693-b989-431c-a8b3-bdeeb0367dc6">RoleForAccessCheck</a> property is defined in the client context, the <b>AccessCheck</b> method will be performed only on that role.

When this method is called, the application group membership is added to the client context so that it does not need to be recomputed for subsequent access checks on the same client context.

This method cannot be called by a BizRule.



