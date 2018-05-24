---
UID: NF:mswmdm.IWMDMStorage3.CreateEmptyMetadataObject
title: IWMDMStorage3::CreateEmptyMetadataObject
author: windows-driver-content
description: The CreateEmptyMetadataObject method creates a new IWMDMMetaData interface. This interface is used to set or retrieve metadata properties of a storage.
old-location: wmdm\iwmdmstorage3_createemptymetadataobject.htm
old-project: WMDM
ms.assetid: e46b5f30-3dd9-4e5a-bd75-c7716a1d8a2a
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: CreateEmptyMetadataObject, CreateEmptyMetadataObject method [windows Media Device Manager], CreateEmptyMetadataObject method [windows Media Device Manager],IWMDMStorage3 interface, IWMDMStorage3 interface [windows Media Device Manager],CreateEmptyMetadataObject method, IWMDMStorage3.CreateEmptyMetadataObject, IWMDMStorage3::CreateEmptyMetadataObject, IWMDMStorage3CreateEmptyMetadataObject, mswmdm/IWMDMStorage3::CreateEmptyMetadataObject, wmdm.iwmdmstorage3_createemptymetadataobject
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
-	IWMDMStorage3.CreateEmptyMetadataObject
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage3::CreateEmptyMetadataObject


## -description



The <b>CreateEmptyMetadataObject</b> method creates a new <b>IWMDMMetaData</b> interface. This interface is used to set or retrieve metadata properties of a storage.




## -parameters




### -param ppMetadata [out]

Receives the new <a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData</a> interface. The caller must release this interface when done with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The metadata interface created is not implicitly connected to the storage that created it; it is merely an empty metadata container. You must submit the interface to a method to set or retrieve metadata values.


#### Examples

The following C++ function sends a file to a device. As part of the transfer, it must add metadata to the storage to specify the new storage type.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
      hr = pStorage-&gt;GetAttributes(&amp;attributes, &amp;format);
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
      CComPtr&lt;IWMDMStorage3&gt; pStorage3;
      hr = pStorage-&gt;QueryInterface(__uuidof(IWMDMStorage3), (void**)(&amp;pStorage3));
      BREAK_HR(hr, "Got an IWMDMStorage3 interface in mySendFile.","Couldn't get an IWMDMStorage3 in mySendFile.");

      // First create the IWMDMMetaData interface.
      IWMDMMetaData* pMetadata;
      hr = pStorage3-&gt;CreateEmptyMetadataObject(&amp;pMetadata);
      BREAK_HR(hr,"Created an IWMDMMetaData interface in mySendFile.","Couldn't create an IWMDMMetaData interface in mySendFile.");

      //
      // Set the file format.
      //
      WMDM_FORMATCODE fileFormat = myGetWMDM_FORMATCODE(pwszFileName);
      hr = pMetadata-&gt;AddItem(WMDM_TYPE_DWORD, g_wszWMDMFormatCode, (BYTE*)&amp;fileFormat, sizeof(WMDM_TYPE_DWORD));


      //
      // Get the proper interface and transfer the file.
      //
      CComPtr&lt;IWMDMStorageControl3&gt; pStgCtl3;
      CComPtr&lt;IWMDMStorage&gt; pNewStorage;
      hr = pStorage-&gt;QueryInterface(__uuidof(IWMDMStorageControl3),(void**)(&amp;pStgCtl3));

      // Get the simple file name to use for the destination file.
      wstring destFile = pwszFileName;
      destFile = destFile.substr(destFile.find_last_of(L"\\") + 1);

      // Get a progress indicator.
      CComQIPtr&lt;IWMDMProgress&gt; pProgress(this);

      // Set the flags for the operation
      UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
         WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
         WMDM_CONTENT_FILE | // We're inserting a file.
         WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
      if (pOperation != NULL)
         flags |= WMDM_CONTENT_OPERATIONINTERFACE;

      // Send the file and metadata.
      hr = pStgCtl3-&gt;Insert3(
         flags,
         WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
         const_cast&lt;WCHAR*&gt;(pwszFileName), // Source file.
         NULL, // Destination file name.
         pOperation, // Null to allow WMDM to read the file; non-null to present raw data bytes to WMDM.
         pProgress, // Interface to send simple progress notifications.
         pMetadata, // IWMDMMetaData interface previously created and filled.
         NULL, 
         &amp;pNewStorage);
      if (FAILED(hr))
         m_pLogger-&gt;LogDword(WMDM_LOG_SEV_ERROR, NULL, "Error calling Insert3 in mySendFile: %lX", hr);
      BREAK_HR(hr, "Wrote a file to the device in mySendFile", "Couldn't write to the device in mySendFile.");

   } while (FALSE); // End of dummy loop

   return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/b62ea18b-c692-464f-a009-727a2924f8b8">IWMDMStorage3 Interface</a>



<a href="https://msdn.microsoft.com/044a6571-8ec0-48af-b105-07c60c25d68a">IWMDMStorageControl3::Insert3</a>



<a href="https://msdn.microsoft.com/478a5412-e8b4-41c8-802f-9c2748dbaeae">Setting Metadata on a File</a>
 

 

