---
UID: NS:cpl.tagCPLINFO
title: tagCPLINFO
author: windows-driver-content
description: Contains resource information and an application-defined value for a dialog box supported by a Control Panel application.
old-location: shell\CPLINFO.htm
old-project: shell
ms.assetid: 707950c9-c242-43b2-b665-c97a89e632c5
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: "*LPCPLINFO, CPLINFO, CPLINFO structure [Windows Shell], _win32_CPLINFO, cpl/CPLINFO, shell.CPLINFO, tagCPLINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: cpl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CPLINFO, *LPCPLINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Cpl.h
api_name:
-	CPLINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



