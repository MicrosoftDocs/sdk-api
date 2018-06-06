---
UID: NF:setupapi.SetupGetLineTextW
title: SetupGetLineTextW function
author: windows-sdk-content
description: The SetupGetLineText function returns the contents of a line in an INF file in a compact form.
old-location: setup\setupgetlinetext.htm
old-project: SetupApi
ms.assetid: ab689e03-5f4f-4f06-bd44-a927e1ab702d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: SetupGetLineText, SetupGetLineText function [Setup API], SetupGetLineTextA, SetupGetLineTextW, _setupapi_setupgetlinetext, setup.setupgetlinetext, setupapi/SetupGetLineText, setupapi/SetupGetLineTextA, setupapi/SetupGetLineTextW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetLineTextW (Unicode) and SetupGetLineTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-setupapi-inf-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupGetLineText
 - SetupGetLineTextA
 - SetupGetLineTextW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupGetLineTextW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetLineText</b> function returns the contents of a line in an INF file in a compact form. The line to retrieve can be specified by an 
<a href="https://msdn.microsoft.com/5b3d32a8-e651-4017-aaa7-b532ec47da53">INFCONTEXT</a> structure returned from a SetupFindLineXXX function, or by explicitly passing in the INF handle, section, and key of the desired line.


## -parameters




### -param Context [in]

Context for a line in an INF file whose text is to be retrieved. This parameter can be <b>NULL</b>. If <i>Context</i> is <b>NULL</b>, <i>InfHandle</i>, <i>Section</i>, and <i>Key</i> must all be specified.



### -param InfHandle [in]

Handle to the INF file to query. This parameter can be <b>NULL</b>. This parameter is used only if <i>Context</i> is <b>NULL</b>. If <i>Context</i> is <b>NULL</b>, <i>InfHandle</i>, <i>Section</i>, and <i>Key</i> must all be specified.



### -param Section [in]

Pointer to a <b>null</b>-terminated string that specifies the section that  contains the key name of the line whose text is to be retrieved. This parameter can be <b>NULL</b>. This parameter is used only if <i>Context</i> is <b>NULL</b>. If <i>Context</i> is <b>NULL</b>, <i>InfHandle</i>, <i>Section</i>, and <i>Key</i> must be specified.



### -param Key [in]

Pointer to a <b>null</b>-terminated string that contains the key name whose associated string is to be retrieved. This parameter can be <b>NULL</b>. This parameter is used only if <i>Context</i> is <b>NULL</b>. If <i>Context</i> is <b>NULL</b>, <i>InfHandle</i>, <i>Section</i>, and <i>Key</i> must be specified.



### -param ReturnBuffer [in, out]

If not <b>NULL</b>, <i>ReturnBuffer</i> points to a buffer in which this function returns the contents of the line. The <b>null</b>-terminated string must not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. See the Remarks section. This parameter can be <b>NULL</b>.



### -param ReturnBufferSize [in]

Size of the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This includes the <b>null</b> terminator. 


### -param RequiredSize [in, out]

If not <b>NULL</b>, points to a variable in which this function returns the required size for the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This includes the <b>null</b> terminator. If <i>ReturnBuffer</i> is specified and the size required is larger than the value specified in the <i>ReturnBufferSize</i> parameter, the function fails and does not store data in the buffer.
 



## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size required to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


This function returns the contents of a line in a compact format. All extraneous white space is removed and multi-line values are converted into a single contiguous string. For example, this line:

<pre class="syntax" xml:space="preserve"><code>HKLM, , PointerClass0, 1 \
; This is a comment
01, 02, 03</code></pre>
would be returned as:

<pre class="syntax" xml:space="preserve"><code>HKLM,,PointerClass0,1,01,02,03</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/ff4b13b6-62ca-48ae-9ddd-e721bde7bd8b">SetupFindFirstLine</a>



<a href="https://msdn.microsoft.com/ba5b3c62-c6b7-4ec1-83e2-45cdc910a34d">SetupFindNextLine</a>



<a href="https://msdn.microsoft.com/c08e22d0-7eb3-4fad-82a6-e9d4f50c4e73">SetupFindNextMatchLine</a>



<a href="https://msdn.microsoft.com/7a1c313b-3150-4f4f-a1e9-0fc9544b97ab">SetupGetLineByIndex</a>
 

 

