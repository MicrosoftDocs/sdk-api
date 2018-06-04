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

# tagNEWCPLINFOA structure


## -description


Contains resource information and an application-defined value for a dialog box supported by a Control Panel application.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The length of the structure, in bytes.


### -field dwFlags

Type: <b>DWORD</b>

This member is ignored.


### -field dwHelpContext

Type: <b>DWORD</b>

This member is ignored.


### -field lData

 


### -field hIcon

Type: <b>HICON</b>

The identifier of the icon that represents the dialog box. This icon is intended to be displayed by the application that controls the Control Panel application.


### -field szName

Type: <b>TCHAR[32]</b>

A null-terminated string that contains the dialog box name. The name is intended to be displayed below the icon.


### -field szInfo

Type: <b>TCHAR[64]</b>

A null-terminated string containing the dialog box description. The description is intended to be displayed when the icon for the dialog box is selected.


### -field szHelpFile

Type: <b>TCHAR[128]</b>

This member is ignored.


#### - lpData

Type: <b>LONG_PTR</b>

A pointer to data defined by the application. When the Control Panel sends the <a href="https://msdn.microsoft.com/68d74372-2fc2-45ed-8f77-574b943d28fa">CPL_DBLCLK</a> and <a href="https://msdn.microsoft.com/4f632b91-8200-42a3-90cc-a98889704ca4">CPL_STOP</a> messages, it passes this value back to your application.


## -remarks



The <a href="https://msdn.microsoft.com/23063e34-9d77-4167-83cd-8561accf0a8d">CPlApplet</a> function of the Control Panel application returns this information to the Control Panel in response to a <a href="https://msdn.microsoft.com/af52889c-7180-4690-8ed1-a0eb0a9dff35">CPL_NEWINQUIRE</a> message.




## -see-also




<a href="https://msdn.microsoft.com/707950c9-c242-43b2-b665-c97a89e632c5">CPLINFO</a>
 

 

