---
UID: NF:wpcapi.IWPCGamesSettings.IsBlocked
title: IWPCGamesSettings::IsBlocked
author: windows-sdk-content
description: Determines whether the specified game is blocked from execution.
old-location: parcon\iwpcgamessettings_isblocked.htm
tech.root: parcon
ms.assetid: a8cdd3ca-8a0d-4e4a-8a54-eb3ddcab52ff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWPCGamesSettings interface,IsBlocked method, IWPCGamesSettings.IsBlocked, IWPCGamesSettings::IsBlocked, IsBlocked, IsBlocked method, IsBlocked method,IWPCGamesSettings interface, parcon.iwpcgamessettings_isblocked, wpcapi/IWPCGamesSettings::IsBlocked
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCGamesSettings.IsBlocked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWPCGamesSettings::IsBlocked


## -description


Determines whether the specified game is blocked from execution.


## -parameters




### -param guidAppID [in]

The GUID associated with the game during install or game scan detection.


### -param pdwReasons [out]

The reason code. For a list of values, see the <a href="https://msdn.microsoft.com/d8ddea59-04be-4d03-a792-866d8f920e17">WPCFLAG_ISBLOCKED</a> enumeration.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -remarks



If <i>guidAppID</i> is not found, the policy will default to unrated and set *<i>pdwReasons</i> to WPCFLAG_ISBLOCKED_NOT_BLOCKED.




## -see-also




<a href="https://msdn.microsoft.com/7509d9ef-d437-406a-8de6-39733499ca0a">IWPCGamesSettings</a>
 

 

