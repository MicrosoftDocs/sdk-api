---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IADsWinNTSystemInfo interface


## -description


The <b>IADsWinNTSystemInfo</b> interface  retrieves the WinNT system information about a computer. Such system information includes user account name, user domain, host name, and the primary domain controller of the host computer.

The <b>IADsWinNTSystemInfo</b> interface is implemented on the <b>WinNTSystemInfo</b> object residing in Activeds.dll, which is included in the standard installation of ADSI for domain-capable editions of Windows. You must explicitly create an instance of the <b>WinNTSystemInfo</b> object to call the methods on the <b>IADsWinNTSystemInfo</b> interface. This requirement means creating an <b>WinNTSystemInfo</b> instance with the  <a href="_com_cocreateinstance">CoCreateInstance</a> function in C/C++.
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




<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/5ba36851-3d03-4179-8cee-dbebe24b7c4e">IADsWinNTSystemInfo Property Methods</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

