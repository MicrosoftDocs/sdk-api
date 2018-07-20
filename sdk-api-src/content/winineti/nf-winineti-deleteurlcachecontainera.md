---
UID: NF:winineti.DeleteUrlCacheContainerA
title: DeleteUrlCacheContainerA function
author: windows-sdk-content
description: Deletes a cache container.
old-location: wininet\deleteurlcachecontainer.htm
old-project: wininet
ms.assetid: 97F46974-9B20-46C6-B742-4BA5C60491DA
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DeleteUrlCacheContainer, DeleteUrlCacheContainer function [WinINet], DeleteUrlCacheContainerA, DeleteUrlCacheContainerW, wininet.deleteurlcachecontainer, winineti/DeleteUrlCacheContainer, winineti/DeleteUrlCacheContainerA, winineti/DeleteUrlCacheContainerW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winineti.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
tech.root: 
req.typenames: INTERNET_AUTH_NOTIFY_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - DeleteUrlCacheContainer
 - DeleteUrlCacheContainerA
 - DeleteUrlCacheContainerW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DeleteUrlCacheContainerA function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Deletes a cache container.


## -parameters




### -param Name

The name of the cache container to delete.


### -param dwOptions

This parameter is reserved and must be 0.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.



