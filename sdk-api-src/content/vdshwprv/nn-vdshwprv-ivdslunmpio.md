---
UID: NN:vdshwprv.IVdsLunMpio
title: IVdsLunMpio (vdshwprv.h)
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a LUN with MPIO extensions.
old-location: base\ivdslunmpio.htm
tech.root: VDS
ms.assetid: 0c7ab50a-306e-44f8-976d-0e65e36b0fea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsLunMpio, IVdsLunMpio interface [VDS], IVdsLunMpio interface [VDS],described, base.ivdslunmpio, vds/IVdsLunMpio, vdshwprv/IVdsLunMpio
ms.topic: interface
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsLunMpio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsLunMpio interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for performing 
   query and configuration operations on a LUN with MPIO extensions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunMpio</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsLunMpio</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLunMpio</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56866ecb-c84b-4297-9bd4-54969501bf9e">GetLoadBalancePolicy</a>
</td>
<td align="left" width="63%">
Returns the current load balance policy on the LUN.</p> (Inherited from <b>IVdsLunMpio</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7cc1abf-c7f2-4260-b9d2-f70128276e1e">GetPathInfo</a>
</td>
<td align="left" width="63%">
Returns an array of <a href="https://msdn.microsoft.com/14444252-11ca-4614-81d1-9a15e76d0186">VDS_PATH_INFO</a> structures, 
     one for each path to the LUN.</p> (Inherited from <b>IVdsLunMpio</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b1f3437-41db-403e-abdb-febbfe90858c">GetSupportedLbPolicies</a>
</td>
<td align="left" width="63%">
Retrieves the load balance policies that are supported by the hardware provider.</p> (Inherited from <b>IVdsLunMpio</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f3eb00a-864e-4fb7-a722-4537e6b8dd42">SetLoadBalancePolicy</a>
</td>
<td align="left" width="63%">
Sets the load balance policy on the LUN.</p> (Inherited from <b>IVdsLunMpio</b>)</td>
</tr>
</table> 


## -remarks



If your provider is an iSCSI provider, or if your provider does not support MPIO, you should not implement the <b>IVdsLunMpio</b> interface. If an iSCSI provider implements this interface, VDS will ignore it, because VDS uses the service's own routines to handle MPIO for iSCSI.




## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

