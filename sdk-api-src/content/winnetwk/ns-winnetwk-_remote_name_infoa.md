---
UID: NS:winnetwk._REMOTE_NAME_INFOA
title: "_REMOTE_NAME_INFOA"
author: windows-sdk-content
description: The REMOTE_NAME_INFO structure contains path and name information for a network resource.
old-location: wnet\remote_name_info_str.htm
tech.root: WNet
ms.assetid: 0cc2ae86-8a46-4e1b-8c28-5904486ffcb5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPREMOTE_NAME_INFOA, REMOTE_NAME_INFO, REMOTE_NAME_INFO structure [Windows Networking (WNet)], REMOTE_NAME_INFOA, REMOTE_NAME_INFOW, _REMOTE_NAME_INFOA, _REMOTE_NAME_INFOW, _win32_remote_name_info_str, winnetwk/REMOTE_NAME_INFO, winnetwk/_REMOTE_NAME_INFOA, winnetwk/_REMOTE_NAME_INFOW, wnet.remote_name_info_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_REMOTE_NAME_INFOW (Unicode) and _REMOTE_NAME_INFOA (ANSI)"
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
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - REMOTE_NAME_INFO
 - _REMOTE_NAME_INFOA
 - _REMOTE_NAME_INFOW
product: Windows
targetos: Windows
req.typenames: REMOTE_NAME_INFOA, *LPREMOTE_NAME_INFOA
req.redist: 
---

# _REMOTE_NAME_INFOA structure


## -description


The
				<b>REMOTE_NAME_INFO</b> structure contains path and name information for a network resource. The structure contains a member that points to a Universal Naming Convention (UNC) name string for the resource, and two members that point to additional network connection information strings.


## -struct-fields




### -field lpUniversalName

Pointer to the null-terminated UNC name string that identifies a network resource.


### -field lpConnectionName

Pointer to a null-terminated string that is the name of a network connection. For more information, see the following Remarks section.


### -field lpRemainingPath

Pointer to a null-terminated name string. For more information, see the following Remarks section.


## -remarks



The 
<b>REMOTE_NAME_INFO</b> structure contains a pointer to a Universal Naming Convention (UNC) name string. A UNC path identifies a network resource in an unambiguous, computer-independent manner. You can pass the path to processes on other computers, allowing those processes to obtain access to the network resource.

UNC names look like this:

<pre class="syntax" xml:space="preserve"><code>\\servername\sharename\path\file
</code></pre>
In addition, if you pass the value of the <b>lpConnectionName</b> member to the 
<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a> function, it enables you to connect a local device to a network resource. You can do this by passing the value of <b>lpConnectionName</b> in the <b>lpRemoteName</b> member of the 
<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a> structure pointed to by the function's <i>lpNetResource</i> parameter.
			

If you append the string pointed to by the <b>lpRemainingPath</b> member of 
<b>REMOTE_NAME_INFO</b> to the local device string, you can pass the resulting string to functions that require a drive-based path.




## -see-also




<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a>



<a href="https://msdn.microsoft.com/36e64c8a-595a-4d41-aa83-592d525c98ee">UNIVERSAL_NAME_INFO</a>



<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/7969ccbb-d1ae-4a1f-8b9c-862cc6ddef1a">Windows Networking Structures</a>
 

 

