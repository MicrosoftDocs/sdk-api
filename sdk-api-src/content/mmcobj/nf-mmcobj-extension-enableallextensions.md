---
UID: NF:mmcobj.Extension.EnableAllExtensions
title: Extension::EnableAllExtensions
author: windows-sdk-content
description: The EnableAllExtensions method determines whether or not all extensions for the extension snap-in are enabled. This method is the programmatic equivalent of the Add all extensions check box in the Snap-In Manager.
old-location: mmc\extension_enableallextensions.htm
old-project: MMC
ms.assetid: eeb4a400-da1e-47b7-bbbf-a601e92ef55b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EnableAllExtensions, EnableAllExtensions method [MMC], EnableAllExtensions method [MMC],Extension interface, EnableAllExtensions method [MMC],Extension object, Extension interface [MMC],EnableAllExtensions method, Extension object [MMC],EnableAllExtensions method, Extension.EnableAllExtensions, Extension::EnableAllExtensions, _slate_extension.enableallextensions_method, mmc.extension_enableallextensions
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
 - Mmcndmgr.dll
api_name:
 - Extension.EnableAllExtensions
 - Extension.EnableAllExtensions
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# Extension::EnableAllExtensions


## -description


The 
<b>EnableAllExtensions</b> method determines whether or not all extensions for the extension snap-in are enabled. This method is the programmatic equivalent of the <b>Add all extensions</b> check box in the Snap-In Manager.


## -parameters




### -param Enable

Value that determines whether all extensions are enabled. To add all available extensions, set <i>Enable</i> to 1. To add or exclude individual extensions, set <i>Enable</i> to 0, and then call 
<a href="https://msdn.microsoft.com/7e060b12-880d-4639-8571-63e237446847">Extension.Enable</a> to enable or disable individual extension snap-ins.


## -returns



This method does not return a value.




## -remarks



The 
<a href="https://msdn.microsoft.com/100e73d3-b40b-4c44-99f0-b72c232b9632">Extension</a> object is a snap-in, and the 
<b>EnableAllExtensions</b> method applies to the extensions that can extend the 
<b>Extension</b> object.


#### Examples

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>objExt.EnableAllExtensions (0)
' This extension's extensions can now be enabled or disabled.
' ...</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7e060b12-880d-4639-8571-63e237446847">Extension.Enable</a>



<a href="https://msdn.microsoft.com/bec3a7f4-1b39-416a-a704-64a267e78e63">Extension.Extensions</a>
 

 

