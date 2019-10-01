---
UID: NS:dsclient.__unnamed_struct_1
title: DSOBJECTNAMES (dsclient.h)
author: windows-sdk-content
description: The DSOBJECTNAMES structure is used to contain directory object data for use by an Active Directory property sheet or context menu extension.
old-location: ad\dsobjectnames.htm
tech.root: ad
ms.assetid: dfc1e88f-40ff-4ec1-9718-4801f678fa3f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDSOBJECTNAMES, DSOBJECTNAMES, DSOBJECTNAMES structure [Active Directory], LPDSOBJECTNAMES, LPDSOBJECTNAMES structure pointer [Active Directory], _glines_dsobjectnames, ad.dsobjectnames, dsclient/DSOBJECTNAMES, dsclient/LPDSOBJECTNAMES"
ms.topic: struct
f1_keywords: 
 - "dsclient/DSOBJECTNAMES"
req.header: dsclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Dsclient.h
api_name:
 - DSOBJECTNAMES
targetos: Windows
req.typenames: DSOBJECTNAMES, *LPDSOBJECTNAMES
req.redist: 
ms.custom: 19H1
---

# DSOBJECTNAMES structure


## -description


The <b>DSOBJECTNAMES</b> structure is used to contain directory object data for use by an Active Directory property sheet or context menu extension.


## -struct-fields




### -field clsidNamespace

Contains the namespace identifier which indicates the origin of the namespace selection. The <b>CLSID_DsFolder</b> value (identical to <b>CLSID_MicrosoftDS</b>) is used to identify namespaces implemented by Active Directory Domain Services.


### -field cItems

Contains the number of elements in the <b>aObjects</b> array.


### -field aObjects

Contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/dsclient/ns-dsclient-dsobject">DSBOJECT</a> structures. Each <b>DSBOJECT</b> structure represents a single directory object. The <b>cItems</b> member contains the number of elements in the array.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/ns-dsclient-dsobject">DSBOJECT</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>
 

 

