---
UID: NF:shldisp.IAutoComplete.Enable
title: IAutoComplete::Enable
author: windows-sdk-content
description: Enables or disables autocompletion.
old-location: shell\IAutoComplete_Enable.htm
tech.root: shell
ms.assetid: dd22d855-6ade-4e30-9d39-a4a6434e7185
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: Enable, Enable method [Windows Shell], Enable method [Windows Shell],IAutoComplete interface, IAutoComplete interface [Windows Shell],Enable method, IAutoComplete.Enable, IAutoComplete::Enable, _win32_IAutoComplete_Enable, shell.IAutoComplete_Enable, shldisp/IAutoComplete::Enable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IAutoComplete.Enable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAutoComplete::Enable


## -description


Enables or disables autocompletion.


## -parameters




### -param fEnable [in]

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> to enable autocompletion, or <b>FALSE</b> to disable it.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



Autocompletion is enabled by default. Applications need only to call this method to disable autocompletion or to reenable it if it has been disabled.




## -see-also




<a href="https://msdn.microsoft.com/bed6eb41-3086-4af7-8c75-651da9dba3b2">IAutoComplete</a>
 

 

