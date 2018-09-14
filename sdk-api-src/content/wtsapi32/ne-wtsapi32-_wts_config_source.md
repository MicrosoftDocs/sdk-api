---
UID: NE:wtsapi32._WTS_CONFIG_SOURCE
title: "_WTS_CONFIG_SOURCE"
author: windows-sdk-content
description: Specifies the source of configuration information returned by the WTSQueryUserConfig function.
old-location: termserv\wts_config_source.htm
tech.root: TermServ
ms.assetid: 2e1f45d9-dc89-4848-9ba5-e6d54b2a7737
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WTSUserConfigSourceSAM, WTS_CONFIG_SOURCE, WTS_CONFIG_SOURCE enumeration [Remote Desktop Services], _WTS_CONFIG_SOURCE, termserv.wts_config_source, wtsapi32/WTSUserConfigSourceSAM, wtsapi32/WTS_CONFIG_SOURCE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - Wtsapi32.h
api_name:
 - WTS_CONFIG_SOURCE
product: Windows
targetos: Windows
req.typenames: WTS_CONFIG_SOURCE
req.redist: 
---

# _WTS_CONFIG_SOURCE enumeration


## -description


Specifies the  source of configuration information returned by the <a href="https://msdn.microsoft.com/aabbcc03-3241-49ab-ab11-ccd3e6893e78">WTSQueryUserConfig</a> function. This enumeration type is used in the <a href="https://msdn.microsoft.com/73788ea3-1ba7-4749-983d-4ca6e4f76acb">WTSUSERCONFIG</a> structure.


## -enum-fields




### -field WTSUserConfigSourceSAM

The configuration information came from the Security Accounts Manager (SAM) database.


## -see-also




<a href="https://msdn.microsoft.com/aabbcc03-3241-49ab-ab11-ccd3e6893e78">WTSQueryUserConfig</a>



<a href="https://msdn.microsoft.com/73788ea3-1ba7-4749-983d-4ca6e4f76acb">WTSUSERCONFIG</a>
 

 

