---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAzNameResolver::NamesFromSids


## -description


The <b>NamesFromSids</b> method gets the display names that correspond to the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs).


## -parameters




### -param vSids [in]

An array of string representations of the SIDs to translate.

This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a string representation of a SID.


### -param pvSidTypes [out]

A pointer to an array of elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumeration that specify the types of SIDs being translated.

This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_I4</b> value that specifies an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumeration.


### -param pvNames [out]

A pointer to an array of strings that contain the display names of the principals that correspond to the SIDs specified by the <i>vSids</i> parameter. 

This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a display name. If a name could not be found for one or more of the SIDs, the corresponding array element contains an empty string.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. If the method cannot find the display names of any of the principals, it returns <b>CO_E_NOMATCHINGNAMEFOUND</b>. For a list of other common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



