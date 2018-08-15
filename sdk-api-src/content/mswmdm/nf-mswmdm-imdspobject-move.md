---
UID: NF:mswmdm.IMDSPObject.Move
title: IMDSPObject::Move
author: windows-sdk-content
description: The Move method moves a file or folder on a media device.
old-location: wmdm\imdspobject_move.htm
old-project: WMDM
ms.assetid: 0b054233-1792-4845-81c9-cf20c81d135f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMDSPObject interface [windows Media Device Manager],Move method, IMDSPObject.Move, IMDSPObject::Move, IMDSPObjectMove, Move, Move method [windows Media Device Manager], Move method [windows Media Device Manager],IMDSPObject interface, mswmdm/IMDSPObject::Move, wmdm.imdspobject_move
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPObject.Move
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPObject::Move


## -description



The <b>Move</b> method moves a file or folder on a media device.




## -parameters




### -param fuMode [in]

Processing mode by which to invoke the <b>Move</b> operation and the method by which to move. Specify exactly one of the following two modes. If both modes are specified, block mode is used.

<table>
<tr>
<th>Mode
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_MODE_BLOCK</td>
<td>The operation will be performed using block mode processing. The call will not return until the operation is finished.</td>
</tr>
<tr>
<td>WMDM_MODE_THREAD</td>
<td>The operation will be performed using thread mode processing. The call will return immediately, and the operation will be performed in a background thread.</td>
</tr>
</table>
 

The following table lists flags that indicate where the object will be moved to. One value from this table is combined with one value from the preceding Mode table by using a bitwise <b>OR</b>.

<table>
<tr>
<th>Method of move
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_INSERTBEFORE</td>
<td>The object will be inserted before the target object.</td>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_INSERTINTO</td>
<td>The object will be inserted into the target object. The target object must be a folder. If the target object is a file, this method fails.</td>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_INSERTAFTER</td>
<td>The object will be inserted after the target object.</td>
</tr>
</table>
 


### -param pProgress [in]

Pointer to an <a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress</a> interface that has been implemented by the application to track the progress of ongoing operations. This parameter is optional and should be set to <b>NULL</b> when not being used.


### -param pTarget [in]

Pointer to the target object before or after which you want to put the current object.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



A file or directory can be moved only within the same root storage. The object on which this method is called must be updated to reflect its new location.

This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/271d7185-1a9d-4bec-9289-4ae5461ed741">IMDSPObject Interface</a>



<a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>
 

 

