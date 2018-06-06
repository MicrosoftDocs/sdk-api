---
UID: NS:ntmsapi._NTMS_COMPUTERINFORMATION
title: "_NTMS_COMPUTERINFORMATION"
author: windows-sdk-content
description: The NTMS_COMPUTERINFORMATION structure defines the properties specific to the RSM server.
old-location: fs\ntms_computerinformation.htm
old-project: Rsm
ms.assetid: 11dd71eb-7193-40d5-b193-4d529eec3ca7
ms.author: windowssdkdev
ms.date: 04/05/2018
ms.keywords: NTMS_COMPUTERINFO, NTMS_COMPUTERINFO structure [Files], NTMS_COMPUTERINFORMATION, NTMS_COMPUTERINFORMATION structure [Files], NTMS_LIBREQFLAGS_NOAUTOPURGE, NTMS_LIBREQFLAGS_NOFAILEDPURGE, NTMS_OPREQFLAGS_NOALERTS, NTMS_OPREQFLAGS_NOAUTOPURGE, NTMS_OPREQFLAGS_NOFAILEDPURGE, NTMS_OPREQFLAGS_NOTRAYICON, NTMS_POOLPOLICY_KEEPOFFLINEIMPORT, NTMS_POOLPOLICY_PURGEOFFLINESCRATCH, _NTMS_COMPUTERINFORMATION, _zaw_ntms_computerinformation, base.ntms_computerinformation, fs.ntms_computerinformation, ntmsapi/NTMS_COMPUTERINFORMATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntmsapi.h
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
req.typenames: NTMS_COMPUTERINFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NTMS_COMPUTERINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _NTMS_COMPUTERINFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_COMPUTERINFORMATION</b> structure defines the properties specific to the RSM server.


## -struct-fields




### -field dwLibRequestPurgeTime

Number of seconds completed library requests are maintained in the work queue.


### -field dwOpRequestPurgeTime

Number of seconds that completed operator requests are maintained in the operator request queue.


### -field dwLibRequestFlags

Library request options. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBREQFLAGS_NOAUTOPURGE"></a><a id="ntms_libreqflags_noautopurge"></a><dl>
<dt><b>NTMS_LIBREQFLAGS_NOAUTOPURGE</b></dt>
</dl>
</td>
<td width="60%">
Library requests are not purged from the work queue. Set to <b>NULL</b> by default.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBREQFLAGS_NOFAILEDPURGE"></a><a id="ntms_libreqflags_nofailedpurge"></a><dl>
<dt><b>NTMS_LIBREQFLAGS_NOFAILEDPURGE</b></dt>
</dl>
</td>
<td width="60%">
Failed work items are not purged from the work queue. Set to <b>NULL</b> by default.

</td>
</tr>
</table>
 


### -field dwOpRequestFlags

Operator request options. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQFLAGS_NOAUTOPURGE"></a><a id="ntms_opreqflags_noautopurge"></a><dl>
<dt><b>NTMS_OPREQFLAGS_NOAUTOPURGE</b></dt>
</dl>
</td>
<td width="60%">
Operator requests are not purged from the work queue. Set to <b>NULL</b> by default.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQFLAGS_NOFAILEDPURGE"></a><a id="ntms_opreqflags_nofailedpurge"></a><dl>
<dt><b>NTMS_OPREQFLAGS_NOFAILEDPURGE</b></dt>
</dl>
</td>
<td width="60%">
Operator requests are not purged from the queue. Set to <b>NULL</b> by default.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQFLAGS_NOALERTS"></a><a id="ntms_opreqflags_noalerts"></a><dl>
<dt><b>NTMS_OPREQFLAGS_NOALERTS</b></dt>
</dl>
</td>
<td width="60%">
The alert pop-up for operator requests is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQFLAGS_NOTRAYICON"></a><a id="ntms_opreqflags_notrayicon"></a><dl>
<dt><b>NTMS_OPREQFLAGS_NOTRAYICON</b></dt>
</dl>
</td>
<td width="60%">
The taskbar icon for operator requests is disabled.

</td>
</tr>
</table>
 


### -field dwMediaPoolPolicy

Media pool policies. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLPOLICY_PURGEOFFLINESCRATCH"></a><a id="ntms_poolpolicy_purgeofflinescratch"></a><dl>
<dt><b>NTMS_POOLPOLICY_PURGEOFFLINESCRATCH</b></dt>
</dl>
</td>
<td width="60%">
Any Free media ejected are automatically deleted. Set to <b>NULL</b> by default.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLPOLICY_KEEPOFFLINEIMPORT"></a><a id="ntms_poolpolicy_keepofflineimport"></a><dl>
<dt><b>NTMS_POOLPOLICY_KEEPOFFLINEIMPORT</b></dt>
</dl>
</td>
<td width="60%">
Any Import media ejected is not deleted automatically. Set to <b>NULL</b> by default.

</td>
</tr>
</table>
 


## -remarks



The 
<b>NTMS_COMPUTERINFORMATION</b> structure is included in the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>
 

 

