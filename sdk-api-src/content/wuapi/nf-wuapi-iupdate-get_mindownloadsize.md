---
UID: NF:wuapi.IUpdate.get_MinDownloadSize
title: IUpdate::get_MinDownloadSize
author: windows-sdk-content
description: Gets the minimum download size of the update.
old-location: wua\iupdate_mindownloadsize.htm
old-project: Wua_Sdk
ms.assetid: 58666d64-fe29-4ece-8b51-67212f90e54e
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IUpdate interface [Windows Update Agent],MinDownloadSize property, IUpdate.MinDownloadSize, IUpdate.get_MinDownloadSize, IUpdate::MinDownloadSize, IUpdate::get_MinDownloadSize, MinDownloadSize property [Windows Update Agent], MinDownloadSize property [Windows Update Agent],IUpdate interface, get_MinDownloadSize, wua.iupdate_mindownloadsize, wuapi/IUpdate::MinDownloadSize, wuapi/IUpdate::get_MinDownloadSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdate.MinDownloadSize
-	IUpdate.get_MinDownloadSize
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdate::get_MinDownloadSize


## -description


Gets the minimum download size of the update.

This property is read-only.


## -parameters


## -remarks



The <b>MinDownloadSize</b> property of an update is always downloaded.  However, the <a href="https://msdn.microsoft.com/22f19d4f-e144-4b06-a428-d2133198288a">MaxDownloadSize</a> property is not always downloaded. The <b>MaxDownloadSize</b> property is downloaded based on the configuration of the computer that receives the update.




## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

