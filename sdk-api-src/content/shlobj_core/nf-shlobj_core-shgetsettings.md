---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SHGetSettings function


## -description


Retrieves the current Shell option settings.


## -parameters




### -param psfs

TBD


### -param dwMask

Type: <b>DWORD</b>

A set of flags that determine which members of <i>lpsfs</i> are being requested. This can be one or more of the following values.



#### SSF_DESKTOPHTML

The <b>fDesktopHTML</b> member is being requested.



#### SSF_DONTPRETTYPATH

The <b>fDontPrettyPath</b> member is being requested.



#### SSF_DOUBLECLICKINWEBVIEW

The <b>fDoubleClickInWebView</b> member is being requested.



#### SSF_HIDEICONS

The <b>fHideIcons</b> member is being requested.



#### SSF_MAPNETDRVBUTTON

The 
						<b>fMapNetDrvBtn</b> member is being requested.



#### SSF_NOCONFIRMRECYCLE

The 
						<b>fNoConfirmRecycle</b> member is being requested.



#### SSF_SHOWALLOBJECTS

The 
						<b>fShowAllObjects</b> member is being requested.



#### SSF_SHOWATTRIBCOL

The 
						<b>fShowAttribCol</b> member is being requested.



<b>Windows Vista:</b> Not used.





#### SSF_SHOWCOMPCOLOR

The 
						<b>fShowCompColor</b> member is being requested.



#### SSF_SHOWEXTENSIONS

The 
						<b>fShowExtensions</b> member is being requested.



#### SSF_SHOWINFOTIP

The 
						<b>fShowInfoTip</b> member is being requested.



#### SSF_SHOWSYSFILES

The 
						<b>fShowSysFiles</b> member is being requested.



#### SSF_WIN95CLASSIC

The 
						<b>fWin95Classic</b> member is being requested.


#### - lpsfs

Type: <b>LPSHELLFLAGSTATE</b>

The address of a <a href="https://msdn.microsoft.com/9968c7c9-79d9-4fb1-bda2-d6a2504cd3a3">SHELLFLAGSTATE</a> structure that receives the Shell option settings.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/d7c2646c-03e0-4d7a-9503-bdf487d43723">SHGetSetSettings</a>
 

 

