---
UID: NF:wuapi.IUpdate.get_LastDeploymentChangeTime
title: IUpdate::get_LastDeploymentChangeTime (wuapi.h)
description: Gets the last published date of the update, in Coordinated Universal Time (UTC) date and time, on the server that deploys the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","LastDeploymentChangeTime property","IUpdate.LastDeploymentChangeTime","IUpdate.get_LastDeploymentChangeTime","IUpdate::LastDeploymentChangeTime","IUpdate::get_LastDeploymentChangeTime","LastDeploymentChangeTime property [Windows Update Agent]","LastDeploymentChangeTime property [Windows Update Agent]","IUpdate interface","get_LastDeploymentChangeTime","wua.iupdate_lastdeploymentchangetime","wuapi/IUpdate::LastDeploymentChangeTime","wuapi/IUpdate::get_LastDeploymentChangeTime"]
old-location: wua\iupdate_lastdeploymentchangetime.htm
tech.root: wua
ms.assetid: 5190ed29-5737-4100-b67c-1333bde28102
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],LastDeploymentChangeTime property, IUpdate.LastDeploymentChangeTime, IUpdate.get_LastDeploymentChangeTime, IUpdate::LastDeploymentChangeTime, IUpdate::get_LastDeploymentChangeTime, LastDeploymentChangeTime property [Windows Update Agent], LastDeploymentChangeTime property [Windows Update Agent],IUpdate interface, get_LastDeploymentChangeTime, wua.iupdate_lastdeploymentchangetime, wuapi/IUpdate::LastDeploymentChangeTime, wuapi/IUpdate::get_LastDeploymentChangeTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdate::get_LastDeploymentChangeTime
 - wuapi/IUpdate::get_LastDeploymentChangeTime
dev_langs:
 - c++
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
---

# IUpdate::get_LastDeploymentChangeTime


## -description

Gets the last published date of the update,  in Coordinated Universal Time (UTC) date and time,  on the server that deploys the update.

This property is read-only.

## -parameters

## -remarks

On computers that are running Windows XP, the <b>LastDeploymentChangeTime</b> property retrieves the same date and time that are retrieved by the  <a href="/previous-versions/windows/desktop/ms750903(v=vs.85)">CreationDate</a> property  of the <b>IUpdateApproval</b> interface. The <a href="/previous-versions/windows/desktop/ms750903(v=vs.85)">CreationDate</a> property is used on computers that are running Windows Server 2003.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>