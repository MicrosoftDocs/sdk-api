---
UID: NF:azroles.IAzObjectPicker.GetPrincipals
title: IAzObjectPicker::GetPrincipals method
author: windows-driver-content
description: Displays a dialog box from which users can choose one or more principals, and then returns the chosen list of principals and their corresponding security identifiers (SIDs).
old-location: security\iazobjectpicker_getprincipals_method.htm
old-project: SecAuthZ
ms.assetid: e03a2160-42bc-44a9-a893-36d2d1de18d4
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetPrincipals method [Security], GetPrincipals method [Security], IAzObjectPicker interface, GetPrincipals,IAzObjectPicker.GetPrincipals, IAzObjectPicker, IAzObjectPicker interface [Security], GetPrincipals method, IAzObjectPicker::GetPrincipals, azroles/IAzObjectPicker::GetPrincipals, security.iazobjectpicker_getprincipals_method
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.h
api_name:
-	IAzObjectPicker.GetPrincipals
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzObjectPicker::GetPrincipals method


## -description


The <b>GetPrincipals</b> method displays a dialog box from which users can choose one or more principals, and then returns the chosen list of principals and their corresponding <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs).


## -parameters




### -param hParentWnd [in]

A handle to the parent window of the dialog box.


### -param bstrTitle [in]

The display title of the dialog box.


### -param pvSidTypes [out]

A pointer to an array of elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumeration that specify the types of the SIDs that correspond to the principals chosen by the user.

This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_I4</b> value that specifies an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumeration.


### -param pvNames [out]

A pointer to an array of display names of the principals chosen by the user. 

This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a display name.


### -param pvSids [out]

A pointer to an array of string representations of the SIDs that correspond to the principals chosen by the user.

This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a string representation of a SID.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



