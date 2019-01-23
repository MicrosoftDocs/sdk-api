---
UID: NF:azroles.IAzObjectPicker.GetPrincipals
title: IAzObjectPicker::GetPrincipals
author: windows-sdk-content
description: Displays a dialog box from which users can choose one or more principals, and then returns the chosen list of principals and their corresponding security identifiers (SIDs).
old-location: security\iazobjectpicker_getprincipals_method.htm
tech.root: SecAuthZ
ms.assetid: e03a2160-42bc-44a9-a893-36d2d1de18d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPrincipals, GetPrincipals method [Security], GetPrincipals method [Security],IAzObjectPicker interface, IAzObjectPicker interface [Security],GetPrincipals method, IAzObjectPicker.GetPrincipals, IAzObjectPicker::GetPrincipals, azroles/IAzObjectPicker::GetPrincipals, security.iazobjectpicker_getprincipals_method
ms.topic: method
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
 - IAzObjectPicker.GetPrincipals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzObjectPicker::GetPrincipals


## -description


The <b>GetPrincipals</b> method displays a dialog box from which users can choose one or more principals, and then returns the chosen list of principals and their corresponding <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs).


## -parameters




### -param hParentWnd [in]

A handle to the parent window of the dialog box.


### -param bstrTitle [in]

The display title of the dialog box.


### -param pvSidTypes [out]

A pointer to an array of elements of the <a href="https://msdn.microsoft.com/4e6af6bd-056b-4f5a-b223-57a673c3fcfa">SID_NAME_USE</a> enumeration that specify the types of the SIDs that correspond to the principals chosen by the user.

This is a variant that contains either a <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> or the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object. Each element of the array holds a <b>VT_I4</b> value that specifies an element of the <a href="https://msdn.microsoft.com/4e6af6bd-056b-4f5a-b223-57a673c3fcfa">SID_NAME_USE</a> enumeration.


### -param pvNames [out]

A pointer to an array of display names of the principals chosen by the user. 

This is a variant that contains either a <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> or the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a display name.


### -param pvSids [out]

A pointer to an array of string representations of the SIDs that correspond to the principals chosen by the user.

This is a variant that contains either a <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> or the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a string representation of a SID.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



