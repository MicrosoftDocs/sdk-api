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

# IExplorerPaneVisibility::GetPaneState


## -description


Gets the visibility state of the given Windows Explorer pane.


## -parameters




### -param ep [in]

Type: <b>REFEXPLORERPANE</b>

A reference to a GUID that uniquely identifies a Windows Explorer pane. One of the following constants as defined in Shlguid.h.



#### EP_NavPane (cb316b22-25f7-42b8-8a09-540d23a43c2f)

The pane on the left side of the Windows Explorer window that hosts the folders tree and <b>Favorites</b>.



#### EP_Commands (d9745868-ca5f-4a76-91cd-f5a129fbb076)

<b>Commands</b> module along the top of the Windows Explorer window.



#### EP_Commands_Organize (72e81700-e3ec-4660-bf24-3c3b7b648806)

<b>Organize</b> menu within the commands module.



#### EP_Commands_View (21f7c32d-eeaa-439b-bb51-37b96fd6a943)

<b>View</b> menu within the commands module.



#### EP_DetailsPane (43abf98b-89b8-472d-b9ce-e69b8229f019)

Pane showing metadata along the bottom of the Windows Explorer window.



#### EP_PreviewPane (893c63d1-45c8-4d17-be19-223be71be365)

Pane on the right of the Windows Explorer window that shows a large reading preview of the file.



#### EP_QueryPane (65bcde4f-4f07-4f27-83a7-1afca4df7ddd)

Quick filter buttons to aid in a search.



#### EP_AdvQueryPane (b4e9db8b-34ba-4c39-b5cc-16a1bd2c411c)

Additional fields and options to aid in a search.



#### EP_StatusBar (65fe56ce-5cfe-4bc4-ad8a-7ae3fe7e8f7c)

<b>Introduced in Windows 8</b>: A status bar that indicates the progress of some process, such as copying or downloading.



#### EP_Ribbon (d27524a8-c9f2-4834-a106-df8889fd4f37)

<b>Introduced in Windows 8</b>: The ribbon, which is the control that replaced menus and toolbars at the top of many Microsoft applications.


### -param peps [out]

Type: <b><a href="https://msdn.microsoft.com/4caa2fe7-5bb3-4940-a429-fd32128eea84">EXPLORERPANESTATE</a>*</b>

When this method returns, contains the visibility state of the given Windows Explorer pane as one of the <a href="https://msdn.microsoft.com/4caa2fe7-5bb3-4940-a429-fd32128eea84">EXPLORERPANESTATE</a> constants.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the implementer does not care about the state of a given pane and therefore does not want to change it, then the implementer should return a success code for the method and EPS_DONTCARE for the <i>peps</i> parameter. If the method fails, it is treated as if EPS_DONTCARE was returned for the <i>peps</i> parameter.



