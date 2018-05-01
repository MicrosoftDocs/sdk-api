---
UID: NF:wiamdef.WIAS_LHRESULT
title: WIAS_LHRESULT macro
author: windows-driver-content
description: The WIAS_LHRESULT macro is obsolete for Windows Vista and later. It is recommended that the WIAS_HRESULT macro be used instead. The WIAS_LHRESULT macro translates an HRESULT value into a string and writes the string to the diagnostic log file.
old-location: image\wias_lhresult.htm
old-project: image
ms.assetid: dcc02735-632f-4b86-ac4f-833c8dcba1c5
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaLog_f9693b87-6464-423a-9b50-f715f3b35f36.xml, WIAS_LHRESULT, WIAS_LHRESULT macro [Imaging Devices], image.wias_lhresult, wiamdef/WIAS_LHRESULT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wiamdef.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me, Windows XP, and later. Obsolete for Windows Vista and later. Use WIAS_HRESULT instead.
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
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiamdef.h
api_name:
-	WIAS_LHRESULT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WIAS_LHRESULT macro


## -description


The WIAS_LHRESULT macro is obsolete for Windows Vista and later. It is recommended that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549572">WIAS_HRESULT</a> macro be used instead. The WIAS_LHRESULT macro translates an HRESULT value into a string and writes the string to the diagnostic log file.


## -parameters




### -param pILog

TBD


### -param hr

Specifies the HRESULT value to be translated into a string.


#### - pIWiaLog

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff543935">IWiaLog Interface</a>.


## -remarks



The following is an example of how the macro can be used:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>hr = wiasFreePropContext(*pContext);
if (hr != S_OK)
   WIAS_LHRESULT(g_pIWiaLog, hr);</pre>
</td>
</tr>
</table></span></div>
The WIAS_LHRESULT macro is not recommended for Windows Vista and later operating system versions. It is recommended that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549572">WIAS_HRESULT</a> macro be used instead. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549572">WIAS_HRESULT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549580">WIAS_LERROR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549600">WIAS_LTRACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549610">WIAS_LWARNING</a>
 

 

