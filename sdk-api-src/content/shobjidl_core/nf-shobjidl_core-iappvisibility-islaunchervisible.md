---
UID: NF:shobjidl_core.IAppVisibility.IsLauncherVisible
title: IAppVisibility::IsLauncherVisible
author: windows-sdk-content
description: Gets a value that indicates whether the Start screen is displayed.
old-location: shell\IAppVisibility_IsLauncherVisible.htm
old-project: shell
ms.assetid: 8D7BBAEC-A745-4707-861E-74CC331ED356
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAppVisibility interface [Windows Shell],IsLauncherVisible method, IAppVisibility.IsLauncherVisible, IAppVisibility::IsLauncherVisible, IsLauncherVisible, IsLauncherVisible method [Windows Shell], IsLauncherVisible method [Windows Shell],IAppVisibility interface, shell.IAppVisibility_IsLauncherVisible, shobjidl_core/IAppVisibility::IsLauncherVisible
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IAppVisibility.IsLauncherVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAppVisibility::IsLauncherVisible


## -description


Gets a value that indicates whether the Start screen is displayed.


## -parameters




### -param pfVisible [out]

<b>TRUE</b> if the Start screen is displayed; otherwise, <b>FALSE.</b>


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pfVisible</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/89E26D36-3536-45F5-9396-83CCFB26890B">IAppVisibility</a>
 

 

