---
UID: NF:fhcfg.IFhConfigMgr.GetDefaultTarget
title: IFhConfigMgr::GetDefaultTarget (fhcfg.h)
author: windows-sdk-content
description: Returns a pointer to an IFhTarget interface that can be used to query information about the currently assigned backup target.
old-location: winprog\ifhconfigmgr_getdefaulttarget.htm
tech.root: DevNotes
ms.assetid: 570CB5FD-7586-41AD-84A6-DA6966B18E91
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FhConfigMgr class [Windows API],GetDefaultTarget method, GetDefaultTarget, GetDefaultTarget method [Windows API], GetDefaultTarget method [Windows API],FhConfigMgr class, GetDefaultTarget method [Windows API],IFhConfigMgr interface, IFhConfigMgr interface [Windows API],GetDefaultTarget method, IFhConfigMgr.GetDefaultTarget, IFhConfigMgr::GetDefaultTarget, fhcfg/IFhConfigMgr::GetDefaultTarget, winprog.ifhconfigmgr_getdefaulttarget
ms.topic: method
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - Fhcfg.h
api_name:
 - IFhConfigMgr.GetDefaultTarget
 - FhConfigMgr.GetDefaultTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFhConfigMgr::GetDefaultTarget


## -description


Returns a pointer to an <a href="https://msdn.microsoft.com/5A73A81A-72A3-4794-86E5-9CA8FCA200C0">IFhTarget</a> interface that can be used to query information about the currently assigned backup target.


## -parameters




### -param DefaultTarget [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/5A73A81A-72A3-4794-86E5-9CA8FCA200C0">IFhTarget</a> interface of an object that represents the currently assigned default target, or <b>NULL</b> if there is no default target.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b>  value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



If no backup target is currently assigned, this method returns <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code>.




## -see-also




<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/5A73A81A-72A3-4794-86E5-9CA8FCA200C0">IFhTarget</a>
 

 

