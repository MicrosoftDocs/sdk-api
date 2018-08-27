---
UID: NF:mmcobj._Application.Hide
title: "_Application::Hide"
author: windows-sdk-content
description: The Hide method hides the MMC application. This method sets the Visible property to False.
old-location: mmc\application_hide.htm
old-project: mmc
ms.assetid: 0ac59101-61ee-48a6-85f8-7aff0ba466b6
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: Application object [MMC],Hide method, Hide, Hide method [MMC], Hide method [MMC],Application object, Hide method [MMC],_Application interface, _Application interface [MMC],Hide method, _Application.Hide, _Application::Hide, _slate_application.hide_method, mmc.application_hide
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmcobj.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MMCObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_PROPERTY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.exe
api_name:
 - Application.Hide
 - _Application.Hide
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmc.exe
req.irql: 
req.product: GDI+ 1.1
---

# _Application::Hide


## -description


The 
<b>Hide</b> method hides the MMC application. This method sets the 
<a href="https://msdn.microsoft.com/438757ad-0ca3-4aab-b955-7c7564028f9f">Visible</a> property to False.


## -parameters






## -returns



This method does not return a value.




## -remarks



This method will fail if the MMC application is under user control. If the 
<a href="https://msdn.microsoft.com/a146a67f-f2d4-4472-adf6-2ab67a3ce353">Application.UserControl</a> property is 1, then the MMC application is under user control.


#### Examples


```vb
' Hide the MMC application.
objMMC.Hide
```





## -see-also




<a href="https://msdn.microsoft.com/17875b21-e102-4755-a1d3-cde141ffe57d">Application.Show</a>



<a href="https://msdn.microsoft.com/a146a67f-f2d4-4472-adf6-2ab67a3ce353">Application.UserControl</a>



<a href="https://msdn.microsoft.com/438757ad-0ca3-4aab-b955-7c7564028f9f">Application.Visible</a>



<a href="https://msdn.microsoft.com/039453b2-736d-4c24-9783-75a30596f3a0">Controlling the Lifetime of an MMC Instance</a>
 

 

