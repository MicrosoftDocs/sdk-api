---
UID: NF:mmc.IRequiredExtensions.GetFirstExtension
title: IRequiredExtensions::GetFirstExtension
author: windows-sdk-content
description: Enables the snap-in to specify the first extension snap-in its list of required extension snap-ins.
old-location: mmc\irequiredextensions_getfirstextension.htm
tech.root: mmc
ms.assetid: 1c84d6ab-c855-4b89-8e36-0794e3ffdb85
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetFirstExtension, GetFirstExtension method [MMC], GetFirstExtension method [MMC],IRequiredExtensions interface, IRequiredExtensions interface [MMC],GetFirstExtension method, IRequiredExtensions.GetFirstExtension, IRequiredExtensions::GetFirstExtension, _slate_irequiredextensions_getfirstextension, mmc.irequiredextensions_getfirstextension, mmc/IRequiredExtensions::GetFirstExtension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - COM
api_location:
 - Mmc.h
api_name:
 - IRequiredExtensions.GetFirstExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRequiredExtensions::GetFirstExtension


## -description


The <b>IRequiredExtensions::GetFirstExtension</b> method enables the snap-in to specify the first extension snap-in its list of required extension snap-ins.


## -parameters




### -param pExtCLSID [out]

A pointer to the CLSID of the first snap-in in the list of required extension snap-ins.


## -returns



This method can return one of these values.




## -remarks



MMC calls this method if 
<a href="https://msdn.microsoft.com/f7278976-8f15-43a4-b9ef-fb1952fdd455">IRequiredExtensions::EnableAllExtensions</a> returns a value that is not S_OK.

If this method returns S_OK, MMC adds the extension snap-in specified by pExtCLSID and then calls 
<a href="https://msdn.microsoft.com/09372a73-e67d-4f1f-805d-b64ca1501976">IRequiredExtensions::GetNextExtension</a> to get the next extension snap-in in the list. If any other value is returned, MMC treats the required list as if it were empty by not adding the extension snap-in specified by pExtCLSID and not calling <b>IRequiredExtensions::GetNextExtension</b>.




## -see-also




<a href="https://msdn.microsoft.com/55832db9-30d9-4a5f-bfef-a014b1050f22">IRequiredExtensions</a>



<a href="https://msdn.microsoft.com/f7278976-8f15-43a4-b9ef-fb1952fdd455">IRequiredExtensions::EnableAllExtensions</a>



<a href="https://msdn.microsoft.com/09372a73-e67d-4f1f-805d-b64ca1501976">IRequiredExtensions::GetNextExtension</a>
 

 

