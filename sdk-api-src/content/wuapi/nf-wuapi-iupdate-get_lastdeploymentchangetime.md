---
UID: NF:wuapi.IUpdate.get_LastDeploymentChangeTime
title: IUpdate::get_LastDeploymentChangeTime (wuapi.h)
author: windows-sdk-content
description: Gets the last published date of the update, in Coordinated Universal Time (UTC) date and time, on the server that deploys the update.
old-location: wua\iupdate_lastdeploymentchangetime.htm
tech.root: Wua_Sdk
ms.assetid: 5190ed29-5737-4100-b67c-1333bde28102
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],LastDeploymentChangeTime property, IUpdate.LastDeploymentChangeTime, IUpdate.get_LastDeploymentChangeTime, IUpdate::LastDeploymentChangeTime, IUpdate::get_LastDeploymentChangeTime, LastDeploymentChangeTime property [Windows Update Agent], LastDeploymentChangeTime property [Windows Update Agent],IUpdate interface, get_LastDeploymentChangeTime, wua.iupdate_lastdeploymentchangetime, wuapi/IUpdate::LastDeploymentChangeTime, wuapi/IUpdate::get_LastDeploymentChangeTime
ms.topic: method
f1_keywords: ["wuapi/IUpdate.LastDeploymentChangeTime"]
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate.LastDeploymentChangeTime
 - IUpdate.get_LastDeploymentChangeTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdate::get_LastDeploymentChangeTime


## -description


Gets the last published date of the update,  in Coordinated Universal Time (UTC) date and time,  on the server that deploys the update.

This property is read-only.


## -parameters


## -remarks



On computers that are running Windows XP, the <b>LastDeploymentChangeTime</b> property retrieves the same date and time that are retrieved by the  <a href="http://go.microsoft.com/fwlink/p/?linkid=121339">CreationDate</a> property  of the <b>IUpdateApproval</b> interface. The <a href="http://go.microsoft.com/fwlink/p/?linkid=121339">CreationDate</a> property is used on computers that are running Windows Server 2003.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
 

 

