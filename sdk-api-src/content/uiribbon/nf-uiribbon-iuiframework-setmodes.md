---
UID: NF:uiribbon.IUIFramework.SetModes
title: IUIFramework::SetModes
author: windows-sdk-content
description: Specifies the application modes to enable.
old-location: windowsribbon\windowsribbon_iuiframework_setmodes.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\setmodes.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUIFramework interface [Windows Ribbon],SetModes method, IUIFramework.SetModes, IUIFramework::SetModes, SetModes, SetModes method [Windows Ribbon], SetModes method [Windows Ribbon],IUIFramework interface, scenicintent_IUIFramework_SetModes, uiribbon/IUIFramework::SetModes, windowsribbon.windowsribbon_iuiframework_setmodes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiribbon.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_VIEWVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIFramework.SetModes
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUIFramework::SetModes


## -description


Specifies the application modes to enable. 
		


## -parameters




### -param iModes

Type: <b>INT32</b>

A bit mask that identifies the modes. 
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A mode indicates the functionality required and, therefore, which elements should be displayed (or 
				hidden) at run time, depending on the state or context of an application. For example, network connectivity 
				may directly impact the functionality of an application and require a "Network" mode of 
				network-related commands whenever a connection is detected.
			

Modes are specified for elements in the Ribbon markup and bound to individual controls at run time.
			

Modes can be applied to a Ribbon <a href="https://msdn.microsoft.com/en-us/library/Dd316894(v=VS.85).aspx">Tab</a> and <a href="https://msdn.microsoft.com/b0d3fcda-7165-40f4-9e57-c7ab88b31711">Group</a>. 
				

<div class="alert"><b>Note</b>  Modes can be applied to <a href="https://msdn.microsoft.com/a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58">Button</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd316859(v=VS.85).aspx">SplitButton</a>, and <a href="https://msdn.microsoft.com/en-us/library/Dd371662(v=VS.85).aspx">DropDownButton</a> controls when hosted in the left 
				column of the Application Menu. 
				</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371467(v=VS.85).aspx">IUIFramework</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371591(v=VS.85).aspx">Markup Elements</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd940486(v=VS.85).aspx">Reconfiguring the Ribbon with Application Modes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 

