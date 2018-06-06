---
UID: NF:mswmdm.IWMDMStorageControl.Insert
title: IWMDMStorageControl::Insert
author: windows-sdk-content
description: The Insert method puts content into the storage on the device.
old-location: wmdm\iwmdmstoragecontrol_insert.htm
old-project: WMDM
ms.assetid: 909b94fd-99de-4e26-87d6-d074a6eb5da3
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWMDMStorageControl interface [windows Media Device Manager],Insert method, IWMDMStorageControl.Insert, IWMDMStorageControl::Insert, IWMDMStorageControlInsert, Insert, Insert method [windows Media Device Manager], Insert method [windows Media Device Manager],IWMDMStorageControl interface, mswmdm/IWMDMStorageControl::Insert, wmdm.iwmdmstoragecontrol_insert
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMDMStorageControl.Insert
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorageControl::Insert


## -description



The <b>Insert</b> method puts content into the storage on the device.




## -parameters




### -param fuMode [in]

A bitwise <b>OR</b> of the following values. The following table lists the processing modes that can be specified in the <i>fuMode</i> parameter. You must specify exactly one of the first two modes, exactly one of the STORAGECONTROL modes, and exactly one of the CONTENT modes. If both WMDM_MODE_BLOCK and WMDM_MODE_THREAD are specified, block mode is used.

<table>
<tr>
<th>
                  Combinations
                </th>
<th>
                  Mode
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>Exactly one of:</td>
<td>WMDM_MODE_BLOCK</td>
<td>The operation is performed using block mode processing. The call will not return until the operation is finished.</td>
</tr>
<tr>
<td></td>
<td>WMDM_MODE_THREAD</td>
<td>The operation is performed using thread mode processing. The call will return immediately, and the operation is performed in a background thread.</td>
</tr>
<tr>
<td>Exactly one of:</td>
<td>WMDM_STORAGECONTROL_INSERTBEFORE</td>
<td>The object is inserted before the current object.</td>
</tr>
<tr>
<td></td>
<td>WMDM_STORAGECONTROL_INSERTAFTER</td>
<td>The object is inserted after the current object.</td>
</tr>
<tr>
<td></td>
<td>WMDM_STORAGECONTROL_INSERTINTO</td>
<td>The object is inserted into the current object. This will only work if the current object is a folder.</td>
</tr>
<tr>
<td>Exactly one of:</td>
<td>WMDM_CONTENT_FILE</td>
<td>The content being inserted is a file.</td>
</tr>
<tr>
<td></td>
<td>WMDM_CONTENT_FOLDER</td>
<td>The content being inserted is a folder. This will not transfer the contents of the folder.</td>
</tr>
<tr>
<td></td>
<td>WMDM_CONTENT_OPERATIONINTERFACE</td>
<td>The content being inserted is an operation interface. The data for the content should be written to the application-implemented <b>IWMDMOperation</b> interface.</td>
</tr>
<tr>
<td>Zero or more of:</td>
<td>WMDM_FILE_CREATE_OVERWRITE</td>
<td>The object will replace the current object.</td>
</tr>
<tr>
<td></td>
<td>WMDM_MODE_QUERY</td>
<td>A test is performed to determine whether the insert operation could succeed, but the insert will not be performed.</td>
</tr>
<tr>
<td></td>
<td>WMDM_MODE_PROGRESS</td>
<td>The method should return progress notifications through <i>pProgress</i>.</td>
</tr>
<tr>
<td>Zero or one of:</td>
<td>WMDM_MODE_TRANSFER_PROTECTED</td>
<td>The insertion is in protected transfer mode.</td>
</tr>
<tr>
<td></td>
<td>WMDM_MODE_TRANSFER_UNPROTECTED</td>
<td>The insertion is in unprotected transfer mode.</td>
</tr>
</table>
 


### -param pwszFile [in]

Pointer to a wide-character <b>null</b>-terminated string indicating where to find the content for the insert operation. This parameter must be <b>NULL</b> if WMDM_CONTENT_OPERATIONINTERFACE is specified in <i>fuMode</i>.


### -param pOperation [in]

Optional pointer to an <a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation</a> interface, to control the transfer of content to a media device. If specified, <i>fuMode</i> must include the WMDM_CONTENT_OPERATIONINTERFACE flag. This parameter must be <b>NULL</b> if WMDM_CONTENT_FILE or WMDM_CONTENT_FOLDER is specified in <i>fuMode</i>.


### -param pProgress [in]

Optional pointer to an <a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress</a> interface to be used by Windows Media Device Manager to report progress back to the application. If this is used, <i>fuMode</i> should include WMDM_MODE_PROGRESS.


### -param ppNewObject [out]

Pointer to an <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface that will contain the new content. The caller must release this interface when finished with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



If the device supports <a href="https://msdn.microsoft.com/044a6571-8ec0-48af-b105-07c60c25d68a">IWMDMStorageControl3::Insert3</a>, that is the preferred method to use.

The name and extension of the object saved on the device will be the same as the name and extension of the source file (if <i>pOperation</i> is <b>NULL</b>).

If the WMDM_MODE_THREAD flag is specified, you should obtain completion status by calling either <a href="https://msdn.microsoft.com/85265eb7-0702-4890-b6cb-b247296fe392">IWMDMProgress2::End2</a> or <a href="https://msdn.microsoft.com/fb09cfa8-1a96-412f-a97a-6cc1638b0c77">IWMDMProgress3::End3</a>. These methods will ensure that the operation is complete and will also return an HRESULT with success or failure information.

The <b>Insert</b> method does not guarantee that the device supports ordered file insertion, but it provides the flags WMDM_STORAGECONTROL_INSERTBEFORE and WMDM_STORAGECONTROL_INSERTAFTER in case it does. If the file system does not support ordering (for instance, FAT32), WMDM_STORAGECONTROL_INSERTBEFORE and WMDM_STORAGECONTROL_INSERTAFTER will simply insert the new storage object at the same level as the current object in the file system hierarchy.

If an application uses WMDM_MODE_THREAD and passes a non-<b>null</b><i>pProgress</i> parameter, the application must ensure that the object to which <i>pProgress</i> belongs is not destroyed until the insert operation completes, because Windows Media Device Manager will send progress notifications to this object. This object can be destroyed only after it receives an End notification. Failure to do this will result in access violations.




## -see-also




<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>



<a href="https://msdn.microsoft.com/bc6cc03c-e13a-45d8-afcb-1fadd5f4dd8e">IWMDMStorageControl2::Insert2</a>



<a href="https://msdn.microsoft.com/044a6571-8ec0-48af-b105-07c60c25d68a">IWMDMStorageControl3::Insert3</a>



<a href="https://msdn.microsoft.com/4b102666-b54b-4b60-b2e9-68def384268e">IWMDMStorageControl::Read</a>



<a href="https://msdn.microsoft.com/66eaed16-032b-4ac0-a768-aded80f10255">Writing Files to the Device</a>
 

 

