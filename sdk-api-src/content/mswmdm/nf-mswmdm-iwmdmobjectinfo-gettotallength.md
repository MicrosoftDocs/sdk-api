---
UID: NF:mswmdm.IWMDMObjectInfo.GetTotalLength
title: IWMDMObjectInfo::GetTotalLength method
author: windows-driver-content
description: The GetTotalLength method retrieves the total play length of the object, in units appropriate to the format. The value returned is the total length regardless of the current settings of the play length and offset.
old-location: wmdm\iwmdmobjectinfo_gettotallength.htm
old-project: WMDM
ms.assetid: ca0e0efc-ff2e-40d6-ace3-5644013bccff
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetTotalLength method [windows Media Device Manager], GetTotalLength method [windows Media Device Manager], IWMDMObjectInfo interface, GetTotalLength,IWMDMObjectInfo.GetTotalLength, IWMDMObjectInfo, IWMDMObjectInfo interface [windows Media Device Manager], GetTotalLength method, IWMDMObjectInfo::GetTotalLength, IWMDMObjectInfoGetTotalLength, mswmdm/IWMDMObjectInfo::GetTotalLength, wmdm.iwmdmobjectinfo_gettotallength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMObjectInfo.GetTotalLength
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IWMDMObjectInfo::GetTotalLength method


## -description



The <b>GetTotalLength</b> method retrieves the total play length of the object, in units appropriate to the format. The value returned is the total length regardless of the current settings of the play length and offset.




## -parameters




### -param pdwLength [out]

Pointer to a <b>DWORD</b> specifying the total length of the file, in units appropriate to the format.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



For playable files, the total length is specified in milliseconds.

For folders or file systems containing playable files, the value returned indicates the total number of playable files in a folder or in the root of a file system.




## -see-also




<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>
 

 

