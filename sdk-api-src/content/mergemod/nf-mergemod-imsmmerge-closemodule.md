---
UID: NF:mergemod.IMsmMerge.CloseModule
title: IMsmMerge::CloseModule
author: windows-sdk-content
description: The CloseModule method closes the currently open Windows Installer merge module. For more information, see the CloseModule method of the Merge object.
old-location: setup\imsmmerge_closemodule.htm
tech.root: msi
ms.assetid: bbe8ab14-3d8e-441c-a9bf-0319a9b3a5de
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CloseModule, CloseModule method, CloseModule method,IMsmMerge interface, IMsmMerge interface,CloseModule method, IMsmMerge.CloseModule, IMsmMerge::CloseModule, _msi_closemodule_function, mergemod/IMsmMerge::CloseModule, setup.imsmmerge_closemodule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge.CloseModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmMerge::CloseModule


## -description


The 
<b>CloseModule</b> method closes the currently open Windows Installer merge module. For more information, see the 
<a href="https://msdn.microsoft.com/a11f72cf-4c4e-4650-95f9-549169452622">CloseModule</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge object</a>. 

<b>IMsmMerge2::CloseDatabase</b>    Mergemod.dll version 2.0 or later.<div> </div>
<a href="https://msdn.microsoft.com/efbb6238-e9e3-4603-896a-75fcff2bb362">IMsmMerge::CloseDatabase</a>      All Mergemod.dll versions.
			


## -parameters






## -returns



The <b>CloseModule</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an error closing the module. The state of the 
<a href="https://msdn.microsoft.com/6cb4b620-88ce-4348-ab72-6d2ed60c6298">IMsmMerge</a> or 
<a href="https://msdn.microsoft.com/cda5698d-4aee-4771-9989-628162b433ef">IMsmMerge2</a> interface is now undefined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No module was open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



Closing a merge module does not affect any errors that have not been retrieved.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

