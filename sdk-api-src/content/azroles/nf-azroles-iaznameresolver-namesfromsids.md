---
UID: NF:azroles.IAzNameResolver.NamesFromSids
title: IAzNameResolver::NamesFromSids
author: windows-sdk-content
description: Gets the display names that correspond to the specified security identifiers (SIDs).
old-location: security\iaznameresolver_namesfromsids_method.htm
old-project: secauthz
ms.assetid: fedf0164-51ca-480c-8e45-443e74fc5b13
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAzNameResolver interface [Security],NamesFromSids method, IAzNameResolver.NamesFromSids, IAzNameResolver::NamesFromSids, NamesFromSids, NamesFromSids method [Security], NamesFromSids method [Security],IAzNameResolver interface, azroles/IAzNameResolver::NamesFromSids, security.iaznameresolver_namesfromsids_method
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzNameResolver.NamesFromSids
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzNameResolver::NamesFromSids


## -description


The <b>NamesFromSids</b> method gets the display names that correspond to the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs).


## -parameters




### -param vSids [in]

An array of string representations of the SIDs to translate.

This is a variant that contains either a <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a string representation of a SID.


### -param pvSidTypes [out]

A pointer to an array of elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumeration that specify the types of SIDs being translated.

This is a variant that contains either a <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_I4</b> value that specifies an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumeration.


### -param pvNames [out]

A pointer to an array of strings that contain the display names of the principals that correspond to the SIDs specified by the <i>vSids</i> parameter. 

This is a variant that contains either a <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a display name. If a name could not be found for one or more of the SIDs, the corresponding array element contains an empty string.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. If the method cannot find the display names of any of the principals, it returns <b>CO_E_NOMATCHINGNAMEFOUND</b>. For a list of other common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



