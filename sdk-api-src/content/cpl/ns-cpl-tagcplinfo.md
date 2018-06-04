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

# tagCPLINFO structure


## -description


Contains resource information and an application-defined value for a dialog box supported by a Control Panel application. The <a href="https://msdn.microsoft.com/23063e34-9d77-4167-83cd-8561accf0a8d">CPlApplet</a> function of the Control Panel application returns this information to the Control Panel in response to a <a href="https://msdn.microsoft.com/daca87b7-f1ee-40f4-95d2-3150b595151e">CPL_INQUIRE</a> message.


## -struct-fields




### -field idIcon

Type: <b>int</b>

The resource identifier of the icon that represents the dialog box.


### -field idName

Type: <b>int</b>

The resource identifier of the string containing the short name for the dialog box. This name is intended to be displayed below the icon.


### -field idInfo

Type: <b>int</b>

The resource identifier of the string containing the description for the dialog box that is intended to be displayed when the application icon is selected.


### -field lData

 




#### - lpData

Type: <b>LONG_PTR</b>

A pointer to data defined by the application. When the Control Panel sends the <a href="https://msdn.microsoft.com/68d74372-2fc2-45ed-8f77-574b943d28fa">CPL_DBLCLK</a> and <a href="https://msdn.microsoft.com/4f632b91-8200-42a3-90cc-a98889704ca4">CPL_STOP</a> messages, it passes this value back to your application.


## -remarks



If the icon or display strings of the dialog box can change based on the state of the computer, you can specify the CPL_DYNAMIC_RES value for the <b>idIcon</b>, <b>idName</b>, or <b>idInfo</b> members rather than specifying a valid resource identifier. This causes the Control Panel to send the <a href="https://msdn.microsoft.com/af52889c-7180-4690-8ed1-a0eb0a9dff35">CPL_NEWINQUIRE</a> message each time it needs the icon and display strings. Using this technique is significantly slower, however, because the Control Panel will need to load your application each time it sends the <b>CPL_NEWINQUIRE</b> message.



