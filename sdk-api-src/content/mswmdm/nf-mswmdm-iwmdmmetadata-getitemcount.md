---
UID: NF:mswmdm.IWMDMMetaData.GetItemCount
title: IWMDMMetaData::GetItemCount (mswmdm.h)
description: The GetItemCount method retrieves the total number of properties held by the interface.
helpviewer_keywords: ["GetItemCount","GetItemCount method [windows Media Device Manager]","GetItemCount method [windows Media Device Manager]","IWMDMMetaData interface","IWMDMMetaData interface [windows Media Device Manager]","GetItemCount method","IWMDMMetaData.GetItemCount","IWMDMMetaData::GetItemCount","IWMDMMetaDataGetItemCount","mswmdm/IWMDMMetaData::GetItemCount","wmdm.iwmdmmetadata_getitemcount"]
old-location: wmdm\iwmdmmetadata_getitemcount.htm
tech.root: WMDM
ms.assetid: 9f7f9661-d632-4502-940b-6d83fc32cdad
ms.date: 12/05/2018
ms.keywords: GetItemCount, GetItemCount method [windows Media Device Manager], GetItemCount method [windows Media Device Manager],IWMDMMetaData interface, IWMDMMetaData interface [windows Media Device Manager],GetItemCount method, IWMDMMetaData.GetItemCount, IWMDMMetaData::GetItemCount, IWMDMMetaDataGetItemCount, mswmdm/IWMDMMetaData::GetItemCount, wmdm.iwmdmmetadata_getitemcount
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
 - IWMDMMetaData::GetItemCount
 - mswmdm/IWMDMMetaData::GetItemCount
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
 - IWMDMMetaData.GetItemCount
---

# IWMDMMetaData::GetItemCount


## -description

The <b>GetItemCount</b> method retrieves the total number of properties held by the interface.

## -parameters

### -param iCount [out]

Pointer to an integer that receives the total number of metadata properties stored by the interface.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method could be used along with <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-querybyindex">QueryByIndex</a> to enumerate all properties on a storage or device.


#### Examples

The following code retrieves the count of properties in an <b>IWMDMMetaData</b> interface (pMetadata) and tries to retrieve them all by index and print them. It uses a custom error handling macro BREAK_HR.


```cpp

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
                        / /TODO: Display the month, day, and year.
                    }
                    break;
                case WMDM_TYPE_GUID:
                    {
                        WCHAR strGuid[64];
                        StringFromGUID2(reinterpret_cast<GUID&>(value),(LPOLESTR)strGuid, 64);
                        / /TODO: Display the GUID.
                    }
                    break;
                default:
                    // TODO: Display a message indicating that the 
                    // application could not understand the returned value type.
                }
            }
            else // Couldn't get the metadata property at index count - 1.
                // TODO: Display a message indicating that the 
                // application couldn't retrieve a value for the index.
        // Clear the WMDM-allocated memory.
        if (value)
            CoTaskMemFree(value);
        }

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-querybyindex">QueryByIndex</a>



<a href="/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>