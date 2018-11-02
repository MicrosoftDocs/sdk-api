---
UID: NS:ddkmapi._DDOPENDIRECTDRAWIN
title: "_DDOPENDIRECTDRAWIN"
author: windows-sdk-content
description: The DDOPENDIRECTDRAWIN structure contains the Microsoft DirectDraw object information.
old-location: display\ddopendirectdrawin.htm
tech.root: display
ms.assetid: 62a15685-5420-46cf-ae50-14bb8d97a3ce
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPDDOPENDIRECTDRAWIN, DDOPENDIRECTDRAWIN, DDOPENDIRECTDRAWIN structure [Display Devices], LPDDOPENDIRECTDRAWIN, LPDDOPENDIRECTDRAWIN structure pointer [Display Devices], _DDOPENDIRECTDRAWIN, ddkmapi/DDOPENDIRECTDRAWIN, ddkmapi/LPDDOPENDIRECTDRAWIN, ddstrcts_bd64cbc2-e2e3-4929-b127-9151f8b45819.xml, display.ddopendirectdrawin"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDOPENDIRECTDRAWIN
product: Windows
targetos: Windows
req.typenames: DDOPENDIRECTDRAWIN, *LPDDOPENDIRECTDRAWIN
req.redist: 
---

# _DDOPENDIRECTDRAWIN structure


## -description


The DDOPENDIRECTDRAWIN structure contains the Microsoft DirectDraw object information. 


## -struct-fields




### -field dwDirectDrawHandle

Contains the DirectDraw handle that was passed down from user mode.


### -field pfnDirectDrawClose

Points to a <a href="https://msdn.microsoft.com/ee581d7b-c3b8-47e5-bae8-348b22ea0f95">pfnDirectDrawClose</a> callback function that is called if the DirectDraw object goes away.


### -field pContext

Contains a value that is passed if the <a href="https://msdn.microsoft.com/ee581d7b-c3b8-47e5-bae8-348b22ea0f95">pfnDirectDrawClose</a> callback is ever called.


## -see-also




<a href="https://msdn.microsoft.com/57e543e3-071c-4d3f-80ee-99648d34737d">DD_DXAPI_OPENDIRECTDRAW</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

