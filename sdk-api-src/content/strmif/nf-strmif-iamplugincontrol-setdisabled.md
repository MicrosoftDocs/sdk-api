---
UID: NF:strmif.IAMPluginControl.SetDisabled
title: IAMPluginControl::SetDisabled
author: windows-sdk-content
description: Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list.
old-location: dshow\iamplugincontrol_setdisabled.htm
old-project: DirectShow
ms.assetid: 3ac4b3b5-0882-4e30-b3fa-1dcee33a74d3
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMPluginControl interface [DirectShow],SetDisabled method, IAMPluginControl.SetDisabled, IAMPluginControl::SetDisabled, SetDisabled, SetDisabled method [DirectShow], SetDisabled method [DirectShow],IAMPluginControl interface, dshow.iamplugincontrol_setdisabled, strmif/IAMPluginControl::SetDisabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IAMPluginControl.SetDisabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMPluginControl::SetDisabled


## -description


Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list.




## -parameters




### -param clsid [in]

The CLSID to add or remove.


### -param disabled [in]

Specifies whether to add or remove the CSLID. If the value is <b>TRUE</b>, the method adds the CLSID to the blocked list. Otherwise, the method removes it from the list.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/66720991-3a3f-4c45-a543-b8050d31fcc3">IAMPluginControl</a>



<a href="https://msdn.microsoft.com/938ba1b0-822e-4871-8786-b7eeee243867">Intelligent Connect</a>
 

 

