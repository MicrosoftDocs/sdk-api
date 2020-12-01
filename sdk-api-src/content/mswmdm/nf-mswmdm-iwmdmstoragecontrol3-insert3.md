---
UID: NF:mswmdm.IWMDMStorageControl3.Insert3
title: IWMDMStorageControl3::Insert3 (mswmdm.h)
description: The Insert3 method puts content into/next to the storage. This method extends IWMDMStorageControl2::Insert2 by allowing the application to explicitly specify the metadata and type of the object being sent.
helpviewer_keywords: ["IWMDMStorageControl3 interface [windows Media Device Manager]","Insert3 method","IWMDMStorageControl3.Insert3","IWMDMStorageControl3::Insert3","IWMDMStorageControl3Insert3","Insert3","Insert3 method [windows Media Device Manager]","Insert3 method [windows Media Device Manager]","IWMDMStorageControl3 interface","mswmdm/IWMDMStorageControl3::Insert3","wmdm.iwmdmstoragecontrol3_insert3"]
old-location: wmdm\iwmdmstoragecontrol3_insert3.htm
tech.root: WMDM
ms.assetid: 044a6571-8ec0-48af-b105-07c60c25d68a
ms.date: 12/05/2018
ms.keywords: IWMDMStorageControl3 interface [windows Media Device Manager],Insert3 method, IWMDMStorageControl3.Insert3, IWMDMStorageControl3::Insert3, IWMDMStorageControl3Insert3, Insert3, Insert3 method [windows Media Device Manager], Insert3 method [windows Media Device Manager],IWMDMStorageControl3 interface, mswmdm/IWMDMStorageControl3::Insert3, wmdm.iwmdmstoragecontrol3_insert3
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMStorageControl3::Insert3
 - mswmdm/IWMDMStorageControl3::Insert3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorageControl3.Insert3
---

# IWMDMStorageControl3::Insert3


## -description

The <b>Insert3</b> method puts content into/next to the storage. This method extends <b>IWMDMStorageControl2::Insert2</b> by allowing the application to explicitly specify the metadata and type of the object being sent.

## -parameters

### -param fuMode [in]

Processing mode used for the <b>Insert3</b> operation. The following table lists the processing modes that can be specified in the <i>fuMode</i> parameter. You must specify exactly one of the first two modes, exactly one of the STORAGECONTROL modes, and exactly one of the CONTENT modes. If both WMDM_MODE_BLOCK and WMDM_MODE_THREAD are specified, block mode is used. Specifying the WMDM_FILE_ATTR* flags in this function is more efficient than calling this function first, then setting these attributes on the file after it has been created or sent.

<table>
<tr>
<th>Combinations
                </th>
<th>Mode
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Exactly one of:</td>
<td>WMDM_MODE_BLOCK</td>
<td>The operation is performed using block mode processing. The call will not return until the operation is finished.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_MODE_THREAD</td>
<td>The operation is performed using thread mode processing. The call will return immediately, and the operation is performed in a background thread.</td>
</tr>
<tr>
<td>Optional</td>
<td>WMDM_MODE_QUERY</td>
<td>A test is performed to determine whether the insert operation could succeed, but the insert will not be performed.</td>
</tr>
<tr>
<td>Exactly one of:</td>
<td>WMDM_STORAGECONTROL_INSERTBEFORE</td>
<td>The object is inserted before the target object.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_STORAGECONTROL_INSERTAFTER</td>
<td>The object is inserted after the target object.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_STORAGECONTROL_INSERTINTO</td>
<td>The object is inserted into the current object. This will only work if the current object is a folder.</td>
</tr>
<tr>
<td>Optional</td>
<td>WMDM_FILE_CREATE_OVERWRITE</td>
<td>The object will replace the target object.</td>
</tr>
<tr>
<td>Exactly one of:</td>
<td>WMDM_CONTENT_FILE</td>
<td>The content being inserted is a file.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_CONTENT_FOLDER</td>
<td>The content being inserted is a folder. This will not transfer the contents of the folder.</td>
</tr>
<tr>
<td>Optional</td>
<td>WMDM_CONTENT_OPERATIONINTERFACE</td>
<td>The application is passing in an <b>IWMDMOperation</b> interface to control data transfer.</td>
</tr>
<tr>
<td>Zero or more of:</td>
<td>WMDM_FILE_ATTR_READONLY</td>
<td>The storage should be set to read-only on the device.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_FILE_ATTR_HIDDEN</td>
<td>The storage should be set to hidden on the device.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_FILE_ATTR_SYSTEM</td>
<td>The storage should be set to system on the device.</td>
</tr>
<tr>
<td>Optional</td>
<td>WMDM_MODE_PROGRESS</td>
<td>The insertion is in progress.</td>
</tr>
<tr>
<td>Optional one of:</td>
<td>WMDM_MODE_TRANSFER_PROTECTED</td>
<td>The insertion is in protected transfer mode.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_MODE_TRANSFER_UNPROTECTED</td>
<td>The insertion is in unprotected transfer mode.</td>
</tr>
</table>

### -param fuType [in]

One of the following types, specifying the current storage.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_FILE_ATTR_FILE</td>
<td>The current storage is a file.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_FOLDER</td>
<td>The current storage is a folder.</td>
</tr>
</table>

### -param pwszFileSource [in]

Pointer to a wide-character, <b>null</b>-terminated string indicating where to find the content for the insert operation. This parameter must be <b>NULL</b> if WMDM_CONTENT_OPERATIONINTERFACE is specified in <i>fuMode</i>. This parameter can be <b>NULL</b> if a playlist or album is being created.

### -param pwszFileDest [in]

Optional name of file on the device. If not specified and the application passes an <b>IWMDMOperation</b> pointer to <i>pOperation</i>, Windows Media Device Manager will request a destination name by calling <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname">IWMDMOperation::GetObjectName</a>. If not specified and the application does not use <i>pOperation</i>, the original file name and extension are used (without the path).

### -param pOperation [in]

Optional pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation</a> interface, to control the transfer of content to a media device. If specified, <i>fuMode</i> must include the WMDM_CONTENT_OPERATIONINTERFACE flag. This parameter must be <b>NULL</b> if WMDM_CONTENT_FILE or WMDM_CONTENT_FOLDER is specified in <i>fuMode</i>.

### -param pProgress [in]

Optional pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress</a> interface to report action progress back to the application. This parameter can be <b>NULL</b>.

### -param pMetaData [in]

Optional pointer to a metadata object. Create a new metadata object by calling <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject">IWMDMStorage3::CreateEmptyMetadataObject</a>. This parameter allows an application to specify metadata (including format) to set on the device during object creation on the device, which is more efficient than setting metadata afterward. You must set the file format (specified by g_wszWMDMFormatCode). If you do not specify the format code of a file when using this method, an MTP device will not show the file as present in its user interface, and non-MTP devices will behave unpredictably.

### -param pUnknown [in]

Optional <b>IUnknown</b> pointer of any custom COM object to be passed to the secure content provider. This makes it possible to pass custom information to a secure content provider if the application has sufficient information about the secure content provider.

### -param ppNewObject [out]

Pointer to an <b>IWMDMStorage</b> interface that will contain the new content. The caller must release this interface when finished with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Although you can set metadata on a storage after sending it to the device, it is more efficient to set this information in the <i>pMetaData</i> parameter of this method. Doing so provides additional information to the device to enable it to transfer and handle the file appropriately (for example, by storing it in the correct place) or display useful information (such as a user-written description of a picture).

To set properties for a Windows Portable Devices (WPD) device, an application would create an <b>IPortableDeviceValues</b> object and set each property into this collection. Then, the application would serialize the collection to a binary large object (BLOB). Once the data is serialized, the application would add it to the <b>IWMDMMetaData</b> referenced by the <i>pMetadata</i> argument using the g_wszWPDPassthroughPropertyValues metadata constant.

If the WMDM_MODE_THREAD flag is specified, you should obtain completion status by calling either <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress2-end2">IWMDMProgress2::End2</a> or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-end3">IWMDMProgress3::End3</a>. These methods will ensure that the operation is complete and will also return an HRESULT with success or failure information.

If an application uses WMDM_MODE_THREAD and passes a non-<b>null</b><i>pProgress</i> parameter, the application must ensure that the object to which <i>pProgress</i> belongs is not destroyed until the read operation completes, because Windows Media Device Manager will send progress notifications to this object. This object can be destroyed only after it receives an end notification. Failure to do this will result in access violations.

When creating a playlist or other reference object, the object being "inserted" actually contains no data but is simply stored on the device as a group of metadata references to other objects (such as music files). Creating such an "abstract" object on the playlist is described in <a href="/windows/desktop/WMDM/creating-a-playlist-on-the-device">Creating a Playlist on the Device</a>.


#### Examples

The following C++ function sends a file to a device. As part of the transfer, it must add metadata to the storage to specify the new storage type.


```cpp

HRESULT mySendFile(LPCWSTR pwszFileName, IWMDMStorage* pStorage, IWMDMOperation* pOperation)
{
   HRESULT hr = S_OK;

   // A dummy loop to handle unrecoverable errors. When we hit an error we
   // can't handle or don't like, we just use a 'break' statement.
   // The custom BREAK_HR macro checks for failed HRESULT values and does this.
   do
   {
      if (pwszFileName == NULL || pStorage == NULL)
      {
         BREAK_HR(E_POINTER,"","Bad pointer passed in.");
         return E_POINTER;
      }

      // Make sure the destination is a folder.
      DWORD attributes = 0;
      _WAVEFORMATEX format;
      hr = pStorage->GetAttributes(&attributes, &format);
      if (!(attributes | WMDM_FILE_ATTR_FOLDER))
      {
         BREAK_HR(E_FAIL, "", "Storage submitted to mySendFile is not a folder.");
         return E_FAIL;
      }

      // Transcode the file
      hr = myTranscodeMethod(pwszFileName);
      BREAK_HR(hr, "Couldn't transcode the file in mySendFile.", "Transcoded the file in mySendFile.");
      //
      // Let's set some metadata in the storage.
      //
      CComPtr<IWMDMStorage3> pStorage3;
      hr = pStorage->QueryInterface(__uuidof(IWMDMStorage3), (void**)(&pStorage3));
      BREAK_HR(hr, "Got an IWMDMStorage3 interface in mySendFile.","Couldn't get an IWMDMStorage3 in mySendFile.");

      // First create the IWMDMMetaData interface.
      IWMDMMetaData* pMetadata;
      hr = pStorage3->CreateEmptyMetadataObject(&pMetadata);
      BREAK_HR(hr,"Created an IWMDMMetaData interface in mySendFile.","Couldn't create an IWMDMMetaData interface in mySendFile.");

      //
      // Set the file format.
      //
      WMDM_FORMATCODE fileFormat = myGetWMDM_FORMATCODE(pwszFileName);
      hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMFormatCode, (BYTE*)&fileFormat, sizeof(WMDM_TYPE_DWORD));


      //
      // Get the proper interface and transfer the file.
      //
      CComPtr<IWMDMStorageControl3> pStgCtl3;
      CComPtr<IWMDMStorage> pNewStorage;
      hr = pStorage->QueryInterface(__uuidof(IWMDMStorageControl3),(void**)(&pStgCtl3));

      // Get the simple file name to use for the destination file.
      wstring destFile = pwszFileName;
      destFile = destFile.substr(destFile.find_last_of(L"\\") + 1);

      // Get a progress indicator.
      CComQIPtr<IWMDMProgress> pProgress(this);

      // Set the flags for the operation.
      UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
         WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
         WMDM_CONTENT_FILE | // We're inserting a file.
         WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
      if (pOperation != NULL)
         flags |= WMDM_CONTENT_OPERATIONINTERFACE;

      // Send the file and metadata.
      hr = pStgCtl3->Insert3(
         flags,
         WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
         const_cast<WCHAR*>(pwszFileName), // Source file.
         NULL, // Destination file name.
         pOperation, // Null to allow Windows Media Device Manager to read 
                     // the file; non-null to present raw data bytes to 
                     // Windows Media Device Manager.
         pProgress, // Interface to send simple progress notifications.
         pMetadata, // IWMDMMetaData interface previously created and filled.
         NULL, 
         &pNewStorage);
      if (FAILED(hr))
         m_pLogger->LogDword(WMDM_LOG_SEV_ERROR, NULL, "Error calling Insert3 in mySendFile: %lX", hr);
      BREAK_HR(hr, "Wrote a file to the device in mySendFile", "Couldn't write to the device in mySendFile.");

   } while (FALSE); // End of dummy loop

   return hr;
}

```

## -see-also

<a href="/windows/desktop/WMDM/creating-a-playlist-on-the-device">Creating a Playlist on the Device</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getstatus">IWMDMDevice::GetStatus</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2">IWMDMStorageControl2::Insert2</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3">IWMDMStorageControl3 Interface</a>



<a href="/windows/desktop/WMDM/writing-files-to-the-device">Writing Files to the Device</a>