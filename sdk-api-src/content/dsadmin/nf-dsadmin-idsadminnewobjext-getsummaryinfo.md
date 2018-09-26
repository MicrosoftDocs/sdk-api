---
UID: NF:dsadmin.IDsAdminNewObjExt.GetSummaryInfo
title: IDsAdminNewObjExt::GetSummaryInfo
author: windows-sdk-content
description: The IDsAdminNewObjExt::GetSummaryInfo method obtains a string that contains a summary of the data gathered by the new object wizard extension page. This string is displayed in the wizard Finish page.
old-location: ad\idsadminnewobjext_getsummaryinfo.htm
tech.root: ad
ms.assetid: 61d97253-360a-4e35-a05a-33315d153c0f
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetSummaryInfo, GetSummaryInfo method [Active Directory], GetSummaryInfo method [Active Directory],IDsAdminNewObjExt interface, IDsAdminNewObjExt interface [Active Directory],GetSummaryInfo method, IDsAdminNewObjExt.GetSummaryInfo, IDsAdminNewObjExt::GetSummaryInfo, _glines_idsadminnewobjext_getsummaryinfo, ad.idsadminnewobjext__getsummaryinfo, ad.idsadminnewobjext_getsummaryinfo, dsadmin/IDsAdminNewObjExt::GetSummaryInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dsadmin.h
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
req.dll: DSAdmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNewObjExt.GetSummaryInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsAdminNewObjExt::GetSummaryInfo


## -description


The <b>IDsAdminNewObjExt::GetSummaryInfo</b> method obtains a string that contains a summary of the data gathered by the new object wizard extension page. This string is displayed in the wizard Finish page.


## -parameters




### -param pBstrText [out]

A pointer to a <b>BSTR</b> value that receives the summary text. To allocate this value, call <a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. The caller must free this memory by calling <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.


## -returns



If the method is successful, <b>S_OK</b> is returned. If the method fails, an OLE-defined error code is returned. If the extension does not provide a summary string, this method should return <b>E_NOTIMPL</b>.




## -remarks



Support of this method is optional. If the extension does not supply summary information, it should return <b>E_NOTIMPL</b> from this method.




## -see-also




<a href="https://msdn.microsoft.com/a9b98647-b801-4a2a-98a4-d57679c07d55">IDsAdminNewObjExt</a>



<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

