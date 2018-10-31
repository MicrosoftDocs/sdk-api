---
UID: NN:atscpsipparser.IAtscPsipParser
title: IAtscPsipParser
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IAtscPsipParser interface retrieves ATSC Program and System Information Protocol (PSIP) tables.
old-location: mstv\iatscpsipparser.htm
tech.root: MSTV
ms.assetid: dbe922b3-b843-4eaa-807d-5608cfbb9686
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAtscPsipParser, IAtscPsipParser interface [Microsoft TV Technologies], IAtscPsipParser interface [Microsoft TV Technologies],described, IAtscPsipParserInterface, atscpsipparser/IAtscPsipParser, mstv.iatscpsipparser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscPsipParser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAtscPsipParser interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IAtscPsipParser</b> interface retrieves ATSC Program and System Information Protocol (PSIP) tables.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAtscPsipParser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAtscPsipParser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAtscPsipParser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9da30d7d-4536-4753-9687-b2c16b560f2d">GetCAT</a>
</td>
<td align="left" width="63%">
Retrieves the conditional access table (CAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e53b93e3-7269-45aa-8b19-75f78fb44c41">GetEAS</a>
</td>
<td align="left" width="63%">
Retrieves the emergency alert message (EAS) table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b88a6728-d772-48b8-aebc-7d4cc133320a">GetEIT</a>
</td>
<td align="left" width="63%">
Retrieves the event information table (EIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6838620a-3dee-468e-bfc8-00757c06263e">GetETT</a>
</td>
<td align="left" width="63%">
Retrieves the extended text table (ETT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abdfb558-aab9-4929-822a-08b35235c22f">GetMGT</a>
</td>
<td align="left" width="63%">
Retrieves the master guide table (MGT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cfa9ec0-a802-4dbe-9997-d0eaac2b71c9">GetPAT</a>
</td>
<td align="left" width="63%">
Retrieves the program association table (PAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd9a3fb0-4bdc-499b-9db9-85dce50dd24b">GetPMT</a>
</td>
<td align="left" width="63%">
Retrieves the program map table (PMT) for a specified PID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aa6476c-9c75-4139-b5bc-6109ff223d98">GetSTT</a>
</td>
<td align="left" width="63%">
Retrieves the system time table (STT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9c25b9e-615d-4223-baf5-f4df2fc1473a">GetTSDT</a>
</td>
<td align="left" width="63%">
Retrieves the transport stream description table (TSDT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3df008e-020f-4ed3-9422-2d5f0f0b865f">GetVCT</a>
</td>
<td align="left" width="63%">
Retrieves the virtual channel table (VCT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a4d4d17-4fc5-481c-bcf8-0f68b2f0a8e2">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the ATSC PSIP parser.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <b>CoCreateInstance</b>. Use the following CLSID:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>3508C064-B94E-420b-A821-20C8096FAADC</pre>
</td>
</tr>
</table></span></div>
This CLSID is not is not published in an SDK header; define a new GUID constant in your application.

You must call <a href="https://msdn.microsoft.com/7a4d4d17-4fc5-481c-bcf8-0f68b2f0a8e2">Initialize</a> before calling any other methods on the object.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

