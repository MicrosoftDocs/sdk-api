---
UID: NF:shobjidl_core.IShellLibrary.SetOptions
title: IShellLibrary::SetOptions
author: windows-sdk-content
description: Sets the library options.
old-location: shell\IShellLibrary_SetOptions.htm
tech.root: shell
ms.assetid: 8bec0c71-3170-4ff9-aa87-4880d6ac7e32
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellLibrary interface [Windows Shell],SetOptions method, IShellLibrary.SetOptions, IShellLibrary::SetOptions, SetOptions, SetOptions method [Windows Shell], SetOptions method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_SetOptions, shell.IShellLibrary_SetOptions, shobjidl_core/IShellLibrary::SetOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IShellLibrary.SetOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLibrary::SetOptions


## -description


Sets the library options.


## -parameters




### -param lofMask [in]

Type: <b><a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a></b>

A bitmask  that specifies   the   <a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a> values  to change in  this call.


### -param lofOptions [in]

Type: <b><a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a></b>

A bitmask that specifies the new value of each  <a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a>  value to change. <b>LIBRARYOPTIONFLAGS</b>  values that are not set in <i>lofMask</i> are not changed by this call.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a> is a bitwise enumerator, which means that more than one option flag can be set.

To change an option value, you must set the option value that you want to change in <i>lofMask</i> and then set or clear the value of the option in <i>lofOptions</i>.


#### Examples

The following example clears the LOF_PINNEDTONAVPANE library option.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
LIBRARYOPTIONFLAGS	maskValue;
LIBRARYOPTIONFLAGS optionValue;
HRESULT	hr = E_FAIL;

// set the maskValue variable to indicate
// which option value to change
maskValue = LOF_PINNEDTONAVPANE;

// set the optionValue variable to indicate
// the new value of the option
optionValue = ~LOF_PINNEDTONAVPANE;

// call the method
hr = library-&gt;SetOptions (maskValue, optionValue);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

