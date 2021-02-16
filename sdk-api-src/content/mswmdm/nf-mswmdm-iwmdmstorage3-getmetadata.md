---
UID: NF:mswmdm.IWMDMStorage3.GetMetadata
title: IWMDMStorage3::GetMetadata (mswmdm.h)
description: The GetMetadata method retrieves the metadata associated with the storage.
helpviewer_keywords: ["GetMetadata","GetMetadata method [windows Media Device Manager]","GetMetadata method [windows Media Device Manager]","IWMDMStorage3 interface","IWMDMStorage3 interface [windows Media Device Manager]","GetMetadata method","IWMDMStorage3.GetMetadata","IWMDMStorage3::GetMetadata","IWMDMStorage3GetMetadata","mswmdm/IWMDMStorage3::GetMetadata","wmdm.iwmdmstorage3_getmetadata"]
old-location: wmdm\iwmdmstorage3_getmetadata.htm
tech.root: WMDM
ms.assetid: 7e436742-fb19-4e8e-98a2-d961c9f0ecbf
ms.date: 12/05/2018
ms.keywords: GetMetadata, GetMetadata method [windows Media Device Manager], GetMetadata method [windows Media Device Manager],IWMDMStorage3 interface, IWMDMStorage3 interface [windows Media Device Manager],GetMetadata method, IWMDMStorage3.GetMetadata, IWMDMStorage3::GetMetadata, IWMDMStorage3GetMetadata, mswmdm/IWMDMStorage3::GetMetadata, wmdm.iwmdmstorage3_getmetadata
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
 - IWMDMStorage3::GetMetadata
 - mswmdm/IWMDMStorage3::GetMetadata
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
 - IWMDMStorage3.GetMetadata
---

# IWMDMStorage3::GetMetadata


## -description

The <b>GetMetadata</b> method retrieves the metadata associated with the storage.

## -parameters

### -param ppMetadata [out]

Pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData</a> pointer associated with a storage. The caller is responsible for calling <b>Release</b> on this interface and all the allocated values when finished with it, as described under "Clearing allocated memory" in <a href="/windows/desktop/WMDM/discovering-device-format-capabilities">Discovering Device Format Capabilities</a>.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method retrieves all metadata associated with the storage. If an application is seeking specific metadata, it might be more efficient to call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata">IWMDMStorage4::GetSpecifiedMetadata</a>.

When retrieving data from a Windows Portable Devices (WPD) device, the data is returned in binary form. The application should de-serialize this data to obtain the actual property values.


#### Examples

The following C++ function retrieves all the metadata associated with a storage.


```cpp

// Function to print out all the metadata associated with a storage.
HRESULT CWMDMController::GetMetadata(IWMDMStorage *pStorage)
{
   HRESULT hr = S_OK;

   // A dummy loop to handle unrecoverable errors. When we hit an error we
   // can't handle or don't like, we just use a 'break' statement.
   // The custom BREAK_HR macro checks for failed HRESULT values and does this.
   do
   {
      CComPtr<IWMDMStorage3> pStorage3;
      CComPtr<IWMDMMetaData> pMetadata;
      hr = pStorage->QueryInterface(__uuidof(IWMDMStorage3), (void**)&pStorage3);
      BREAK_HR(hr, "Got an IWMDMStorage3 interface in GetMetadata.", "Couldn't get an IWMDMStorage3 interface in GetMetadata.");

      hr = pStorage3->GetMetadata(&pMetadata);
      BREAK_HR(hr, "Got an IWMDMMetaData interface in GetMetadata.", "Couldn't get an IWMDMMetaData interface in GetMetadata.");

      //
      // Loop through all metadata properties, and print out the value of each.
      //
      BYTE* value;
      WMDM_TAG_DATATYPE type;
      UINT len = 0;
      UINT count = 0;
      WCHAR* name;
      // Get the number of metadata items.
      hr = pMetadata->GetItemCount(&count);

      BREAK_HR(hr, "Got a metadata count in GetMetadata.", "Couldn't get a metadata count in GetMetadata.");
      for(;count > 0; count--)
      {
         // Get the metadata property by index.
         WCHAR* name;
         hr = pMetadata->QueryByIndex(count-1, &name, &type, &value, &len);
         if (SUCCEEDED(hr))
         {
            // TODO: Display the property name.
            CoTaskMemFree(name);

            // Print out the value of the property, according to the value type.
            switch (type)
            {
            case WMDM_TYPE_QWORD:
            case WMDM_TYPE_DWORD:
            case WMDM_TYPE_WORD:
               // TODO: Display the value.
               break;
            case WMDM_TYPE_STRING:
               // TODO: Display the value.
               // Release the method-allocated property value memory.
                    if (SUCCEEDED(hr))
                        CoTaskMemFree(value);
               break;
            case WMDM_TYPE_BOOL:
               // TODO: Display the value.
               break;
            case WMDM_TYPE_BINARY:
               // TODO: Display the value.
               break;
            case WMDM_TYPE_DATE:
               {
                  WMDMDATETIME *val = (WMDMDATETIME*)value;
                        // TODO: Display the month, day, and year.
               }
               break;
            case WMDM_TYPE_GUID:
               {
                  WCHAR strGuid[64];
                  StringFromGUID2(reinterpret_cast<GUID&>(value),(LPOLESTR)strGuid, 64);
                  // TODO: Display the GUID value.
               }
               break;
            default:
               // TODO: Display the message: "Could not understand the returned value type
            }
         }
         else // Couldn't get the metadata property at index count - 1.
            // TODO: Display the message: 
            // "Couldn't get a value for index " 
            // followed by the current index value.
      }

      // Now get a specific property by name.
      // If this property isn't supported, the method returns E_INVALIDARG.
      hr = pMetadata->QueryByName(g_wszWMDMFileName, &type, &value, &len);
      if (hr == S_OK) 
      {
         wstring wstr((wchar_t*)value, len / 2); // Create a string from the name.
            // TODO: Display the file name.
            CoTaskMemFree(value);
      }

      // See if file is DRM-protected.
      hr = pMetadata->QueryByName(g_wszWMDMIsProtected, &type, &value, &len);
      if (hr == S_OK)
      {
         // TODO: Display a message that the object is DRM protected.
      }


   }while(FALSE);// End of dummy loop.

   // Clean up and return.
   return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3">IWMDMStorage3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata">IWMDMStorage3::SetMetadata</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata">IWMDMStorage4::GetSpecifiedMetadata</a>