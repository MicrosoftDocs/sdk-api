---
UID: NF:tspubplugin2com.ItsPubPlugin2.ResolvePersonalDesktop
title: ItsPubPlugin2::ResolvePersonalDesktop (tspubplugin2com.h)
description: Called to resolve a mapping between the specified user and a virtual machine in a personal virtual desktop collection.
helpviewer_keywords: ["ItsPubPlugin2 interface [Remote Desktop Services]","ResolvePersonalDesktop method","ItsPubPlugin2.ResolvePersonalDesktop","ItsPubPlugin2::ResolvePersonalDesktop","ResolvePersonalDesktop","ResolvePersonalDesktop method [Remote Desktop Services]","ResolvePersonalDesktop method [Remote Desktop Services]","ItsPubPlugin2 interface","termserv.itspubplugin2_resolvepersonaldesktop","tspubplugin2com/ItsPubPlugin2::ResolvePersonalDesktop"]
old-location: termserv\itspubplugin2_resolvepersonaldesktop.htm
tech.root: TermServ
ms.assetid: 1f88d7a6-c662-4a14-a288-9c346c8fb7f1
ms.date: 12/05/2018
ms.keywords: ItsPubPlugin2 interface [Remote Desktop Services],ResolvePersonalDesktop method, ItsPubPlugin2.ResolvePersonalDesktop, ItsPubPlugin2::ResolvePersonalDesktop, ResolvePersonalDesktop, ResolvePersonalDesktop method [Remote Desktop Services], ResolvePersonalDesktop method [Remote Desktop Services],ItsPubPlugin2 interface, termserv.itspubplugin2_resolvepersonaldesktop, tspubplugin2com/ItsPubPlugin2::ResolvePersonalDesktop
req.header: tspubplugin2com.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tspubplugin2com.idl
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
 - ItsPubPlugin2::ResolvePersonalDesktop
 - tspubplugin2com/ItsPubPlugin2::ResolvePersonalDesktop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tspubplugin2com.h
api_name:
 - ItsPubPlugin2.ResolvePersonalDesktop
---

# ItsPubPlugin2::ResolvePersonalDesktop


## -description

Called to resolve a mapping between the specified user and a virtual machine in a personal virtual desktop collection.

## -parameters

### -param userId [in]

A null-terminated string that contains the security identifier (SID) of the user.

### -param poolId [in]

A null-terminated string that contains the identifier of the collection to obtain the personal desktop from or create the personal desktop in.

### -param ePdResolutionType [in]

A value of the <a href="/windows/win32/api/tspubplugin2com/ne-tspubplugin2com-tspub_plugin_pd_resolution_type">TSPUB_PLUGIN_PD_RESOLUTION_TYPE</a> enumeration that specifies the type of resolution being requested.

### -param pPdAssignmentType [out]

A value of the <a href="/windows/win32/api/tspubplugin2com/ne-tspubplugin2com-tspub_plugin_pd_assignment_type">TSPUB_PLUGIN_PD_ASSIGNMENT_TYPE</a> enumeration that specifies what type of assignment was made for the personal desktop.

### -param endPointName [out]

A null-terminated string that receives the name of the end point for the desktop. The length of this string is limited to <b>MAX_ENDPOINT_SIZE</b> characters, including the terminating <b>NULL</b> character.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>MAX_ENDPOINT_SIZE</b> is declared as follows:

<code>#define MAX_ENDPOINT_SIZE 256</code>

## -see-also

<a href="/windows/desktop/api/tspubplugin2com/nn-tspubplugin2com-itspubplugin2">ItsPubPlugin2</a>