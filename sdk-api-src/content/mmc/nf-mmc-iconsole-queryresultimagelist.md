---
UID: NF:mmc.IConsole.QueryResultImageList
title: IConsole::QueryResultImageList
author: windows-sdk-content
description: Retrieves the console-provided result-view image list. This image list should be used only if the snap-in is using the default list view.
old-location: mmc\iconsole_queryresultimagelist.htm
tech.root: mmc
ms.assetid: 86F2A9ED-4023-4425-8C0A-7593660C623C
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IConsole interface [MMC],QueryResultImageList method, IConsole.QueryResultImageList, IConsole::QueryResultImageList, QueryResultImageList, QueryResultImageList method [MMC], QueryResultImageList method [MMC],IConsole interface, mmc.iconsole_queryresultimagelist, mmc/IConsole::QueryResultImageList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsole.QueryResultImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsole::QueryResultImageList


## -description


Retrieves the console-provided result-view image list. This image list should be used only if the snap-in is using the default list view.


## -parameters




### -param ppImageList [out]

Address of a variable that receives the 
<a href="https://msdn.microsoft.com/a957239b-6cb2-4101-adeb-e9ba4f876af4">IImageList</a> interface pointer.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt300830(v=VS.85).aspx">IConsole</a>



<a href="https://msdn.microsoft.com/a957239b-6cb2-4101-adeb-e9ba4f876af4">IImageList</a>
 

 

