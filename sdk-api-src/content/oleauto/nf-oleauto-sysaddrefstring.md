---
UID: NF:oleauto.SysAddRefString
title: SysAddRefString function
author: windows-sdk-content
description: Increases the pinning reference count for the specified string by one.
old-location: automat\sysaddrefstring.htm
old-project: automat
ms.assetid: 9AE274F1-1517-4D55-B9AE-D75169404880
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: SysAddRefString, SysAddRefString function [Automation], automat.sysaddrefstring, oleauto/SysAddRefString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleaut32.dll
api_name:
 - SysAddRefString
product: Windows
targetos: Windows
req.lib: Mincore.lib
req.dll: Oleaut32.dll
req.irql: 
req.product: ADAM
---

# SysAddRefString function


## -description


<div class="alert"><b>Note</b>  You should only call <b>SysAddRefString</b> if you are implementing a scripting engine that needs to guard against running potentially malicious scripts.</div><div> </div>Increases the  pinning reference count for the specified string by one.


## -parameters




### -param bstrString [in]

The string for which the pinning reference count should increase. While that count remains greater than 0, the memory for the string is prevented from being freed by calls to the <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Strings with the <b>BSTR</b> data type have not traditionally had a reference count. All existing usage of these strings will continue to work with no changes. The <b>SysAddRefString</b> and <a href="https://msdn.microsoft.com/D4905794-A4EA-4925-A4B2-92C8BF6EDFD0">SysReleaseString</a> functions add the ability to use reference counting to pin the string into memory before calling from an untrusted script into an <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> method that may not expect the script to free that memory before the method returns, so that the script cannot force the code for that method into accessing memory that has been freed. After such a method safely returns, the pinning references should be released by calling <b>SysReleaseString</b>.




## -see-also




<a href="https://msdn.microsoft.com/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>



<a href="https://msdn.microsoft.com/D4905794-A4EA-4925-A4B2-92C8BF6EDFD0">SysReleaseString</a>
 

 

