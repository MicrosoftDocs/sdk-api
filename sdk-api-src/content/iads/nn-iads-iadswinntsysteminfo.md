---
UID: NN:iads.IADsWinNTSystemInfo
title: IADsWinNTSystemInfo
author: windows-sdk-content
description: The IADsWinNTSystemInfo interface retrieves the WinNT system information about a computer. Such system information includes user account name, user domain, host name, and the primary domain controller of the host computer.
old-location: adsi\iadswinntsysteminfo.htm
tech.root: ADSI
ms.assetid: 63a20250-1b93-49df-b7f8-7169db8efde0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsWinNTSystemInfo, IADsWinNTSystemInfo interface [ADSI], IADsWinNTSystemInfo interface [ADSI],described, _ds_iadswinntsysteminfo, adsi.iadswinntsysteminfo, iads/IADsWinNTSystemInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsWinNTSystemInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsWinNTSystemInfo interface


## -description


The <b>IADsWinNTSystemInfo</b> interface  retrieves the WinNT system information about a computer. Such system information includes user account name, user domain, host name, and the primary domain controller of the host computer.

The <b>IADsWinNTSystemInfo</b> interface is implemented on the <b>WinNTSystemInfo</b> object residing in Activeds.dll, which is included in the standard installation of ADSI for domain-capable editions of Windows. You must explicitly create an instance of the <b>WinNTSystemInfo</b> object to call the methods on the <b>IADsWinNTSystemInfo</b> interface. This requirement means creating an <b>WinNTSystemInfo</b> instance with the  <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function in C/C++.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsWinNTSystemInfo *pNTsys;
HRESULT hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IADsWinNTSystemInfo,
                              (void**)&amp;pNTsys);</pre>
</td>
</tr>
</table></span></div>You can also use the <b>New</b> operator in Visual Basic.
<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim ntSys As New WinNTSystemInfo</pre>
</td>
</tr>
</table></span></div>You can also call the <b>CreateObject</b> function in a scripting environment, supplying "WinNTSystemInfo" as the ProgID.
<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim ntSys
Set ntSys = CreateObject("WinNTSystemInfo")</pre>
</td>
</tr>
</table></span></div>

## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/5ba36851-3d03-4179-8cee-dbebe24b7c4e">IADsWinNTSystemInfo Property Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

