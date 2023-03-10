---
UID: NF:mswmdm.IWMDMStorage3.CreateEmptyMetadataObject
title: IWMDMStorage3::CreateEmptyMetadataObject (mswmdm.h)
description: The CreateEmptyMetadataObject method creates a new IWMDMMetaData interface. This interface is used to set or retrieve metadata properties of a storage.
helpviewer_keywords: ["CreateEmptyMetadataObject","CreateEmptyMetadataObject method [windows Media Device Manager]","CreateEmptyMetadataObject method [windows Media Device Manager]","IWMDMStorage3 interface","IWMDMStorage3 interface [windows Media Device Manager]","CreateEmptyMetadataObject method","IWMDMStorage3.CreateEmptyMetadataObject","IWMDMStorage3::CreateEmptyMetadataObject","IWMDMStorage3CreateEmptyMetadataObject","mswmdm/IWMDMStorage3::CreateEmptyMetadataObject","wmdm.iwmdmstorage3_createemptymetadataobject"]
old-location: wmdm\iwmdmstorage3_createemptymetadataobject.htm
tech.root: WMDM
ms.assetid: e46b5f30-3dd9-4e5a-bd75-c7716a1d8a2a
ms.date: 12/05/2018
ms.keywords: CreateEmptyMetadataObject, CreateEmptyMetadataObject method [windows Media Device Manager], CreateEmptyMetadataObject method [windows Media Device Manager],IWMDMStorage3 interface, IWMDMStorage3 interface [windows Media Device Manager],CreateEmptyMetadataObject method, IWMDMStorage3.CreateEmptyMetadataObject, IWMDMStorage3::CreateEmptyMetadataObject, IWMDMStorage3CreateEmptyMetadataObject, mswmdm/IWMDMStorage3::CreateEmptyMetadataObject, wmdm.iwmdmstorage3_createemptymetadataobject
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
 - IWMDMStorage3::CreateEmptyMetadataObject
 - mswmdm/IWMDMStorage3::CreateEmptyMetadataObject
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
 - IWMDMStorage3.CreateEmptyMetadataObject
---

# IWMDMStorage3::CreateEmptyMetadataObject


## -description

The <b>CreateEmptyMetadataObject</b> method creates a new <b>IWMDMMetaData</b> interface. This interface is used to set or retrieve metadata properties of a storage.

## -parameters

### -param ppMetadata [out]

Receives the new <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData</a> interface. The caller must release this interface when done with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The metadata interface created is not implicitly connected to the storage that created it; it is merely an empty metadata container. You must submit the interface to a method to set or retrieve metadata values.


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

      // Set the flags for the operation
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
         pOperation, // Null to allow WMDM to read the file; non-null to present raw data bytes to WMDM.
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

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3">IWMDMStorage3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3">IWMDMStorageControl3::Insert3</a>



<a href="/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>