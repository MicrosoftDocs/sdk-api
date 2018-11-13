---
UID: NF:mprapi.MprConfigServerDisconnect
title: MprConfigServerDisconnect function
author: windows-sdk-content
description: The MprConfigServerDisconnect function disconnects a connection made by a previous call to MprConfigServerConnect.
old-location: rras\mprconfigserverdisconnect.htm
tech.root: rras
ms.assetid: 71cdb26b-e9d0-414c-aff9-0eed187d08ba
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MprConfigServerDisconnect, MprConfigServerDisconnect function [RAS], _mpr_mprconfigserverdisconnect, mprapi/MprConfigServerDisconnect, rras.mprconfigserverdisconnect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigServerDisconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprConfigServerDisconnect function


## -description


The 
<b>MprConfigServerDisconnect</b> function disconnects a connection made by a previous call to 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


## -parameters




### -param hMprConfig [in]

Handle to a router configuration obtained from a previous call to 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

