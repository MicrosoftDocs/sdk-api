---
UID: NF:powrprof.EnumPwrSchemes
title: EnumPwrSchemes function (powrprof.h)
author: windows-sdk-content
description: Enumerates all power schemes.
old-location: base\enumpwrschemes.htm
tech.root: power
ms.assetid: 5e9e10b4-84c3-40ec-8de9-220d13795403
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumPwrSchemes, EnumPwrSchemes function, _win32_enumpwrschemes, base.enumpwrschemes, powrprof/EnumPwrSchemes
ms.topic: function
req.header: powrprof.h
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
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - EnumPwrSchemes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EnumPwrSchemes function


## -description


<p class="CCE_Message">[<b>EnumPwrSchemes</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> instead.]

Enumerates all power schemes. For each power scheme enumerated, the function calls a callback function with information about the power scheme.


## -parameters




### -param lpfn [in]

A pointer to a callback function to be called for each power scheme enumerated. For more information, see Remarks.


### -param lParam [in]

A user-defined value to be passed to the callback function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



For each power scheme enumerated, the callback function is called with the following parameters:

<pre class="syntax" xml:space="preserve"><code>
typedef BOOLEAN (CALLBACK* PWRSCHEMESENUMPROC)(
  UINT uiIndex,      // power scheme index
  DWORD dwName,      // size of the sName string, in bytes
  LPWSTR sName,      // name of the power scheme
  DWORD dwDesc,      // size of the sDesc string, in bytes
  LPWSTR sDesc,      // description string
  PPOWER_POLICY pp,  // receives the power policy
  LPARAM lParam      // user-defined value
);</code></pre>
The <i>sName</i> and <i>sDesc</i> parameters are null-terminated Unicode strings. The <i>pp</i> parameter is a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-_power_policy">POWER_POLICY</a> structure containing the power policy scheme. To continue until all power schemes have been enumerated, the callback function must return <b>TRUE</b>. To stop the enumeration, the callback function must return <b>FALSE</b>.

For more information on using PowrProf.h, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-_power_policy">POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>
 

 

