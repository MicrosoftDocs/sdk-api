---
UID: NF:mergemod.IMsmMerge.Connect
title: IMsmMerge::Connect
author: windows-sdk-content
description: The Connect method connects a module that has been, or will be, merged into the database to an additional feature. For more information, see the Connect method of the Merge object.
old-location: setup\imsmmerge_connect.htm
tech.root: msi
ms.assetid: f491beb8-90f7-4e41-891d-ef674306339d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: Connect, Connect method, Connect method,IMsmMerge interface, IMsmMerge interface,Connect method, IMsmMerge.Connect, IMsmMerge::Connect, _msi_connect_function, mergemod/IMsmMerge::Connect, setup.imsmmerge_connect
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
 - IMsmMerge.Connect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mergemod.h
: 
- IMsmMerge.Connect
: 
---

# IMsmMerge::Connect


## -description


The 
<b>Connect</b> method connects a module that has been, or will be, merged into the database to an additional feature. For more information, see the 
<a href="https://msdn.microsoft.com/1c1ef664-792c-4cdc-b468-1ffe0b7810a5">Connect</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object. 

<b>IMsmMerge2::Connect</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::Connect</b>      All Mergemod.dll versions.
			
			


## -parameters




### -param Feature [in]

The name of a feature in the database. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The connect failed.

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



The feature must exist before this function is called. Errors may be retrieved using 
<a href="https://msdn.microsoft.com/81bf84f6-d469-47b1-9097-8a3ee9c8550d">get_Errors</a>. Errors and informational messages are posted to the current log file.

Changes made to the database are not be saved to disk unless 
<a href="https://msdn.microsoft.com/efbb6238-e9e3-4603-896a-75fcff2bb362">CloseDatabase</a> function is called with <i>bCommit</i> set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

