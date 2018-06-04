---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D11Device3::ReadFromSubresource


## -description



          Copies data from a
          <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE_DEFAULT</a>
          texture which was mapped using
          ID3D11DeviceContext3::<a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">Map</a>
          while providing a NULL
          <a href="https://msdn.microsoft.com/cbbb8689-0a7d-43b9-bde3-29d93cc7f0fe">D3D11_MAPPED_SUBRESOURCE</a>
          parameter.
        


## -parameters




### -param pDstData [out]

Type: <b>void*</b>


            A pointer to the destination data in memory.
          


### -param DstRowPitch [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            The size of one row of the destination data.
          


### -param DstDepthPitch [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            The size of one depth slice of destination data.
          


### -param pSrcResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>


            A pointer to the source resource (see
            <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>).
          


### -param SrcSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            A zero-based index, that identifies the destination subresource.
            For more details, see
            <a href="https://msdn.microsoft.com/643a21f7-3c2e-4d62-9236-051f51d31241">D3D11CalcSubresource</a>.
          


### -param pSrcBox [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0cc98805-a36e-41aa-a24f-51fbcf5070df">D3D11_BOX</a>*</b>


              A pointer to a box that defines the portion of the destination subresource to copy the resource data from.
              If NULL, the data is read from the destination subresource with no offset.
              The dimensions of the destination must fit the destination (see
              <a href="https://msdn.microsoft.com/0cc98805-a36e-41aa-a24f-51fbcf5070df">D3D11_BOX</a>).
            


              An empty box results in a no-op.
              A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value.
              When the box is empty, this method doesn't perform any operation.
            


## -returns




            This method does not return a value.
          




## -remarks




          The provided resource must be a
          <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE_DEFAULT</a>
          texture which was mapped for writing by a previous call to
          ID3D11DeviceContext3::<a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">Map</a>
          while providing a NULL
          <a href="https://msdn.microsoft.com/cbbb8689-0a7d-43b9-bde3-29d93cc7f0fe">D3D11_MAPPED_SUBRESOURCE</a>
          parameter.
        


          This API is intended for calling at high frequency.
          Callers can reduce memory by making iterative calls that update progressive regions of the texture, while provide a small buffer during each call.
          It is most efficient to specify large enough regions, though, because this enables D3D to fill whole cache lines in the texture before returning.
        


          For efficiency, ensure the bounds and alignment of the extents within the box are ( 64 / [Bytes per pixel] ) pixels horizontally.
          Vertical bounds and alignment should be 2 rows, except when 1-byte-per-pixel formats are used, in which case 4 rows are recommended.
          Single depth slices per call are handled efficiently.
          It is recommended but not necessary to provide pointers and strides which are 128-byte aligned.
        


          When reading from sub mipmap levels, it is recommended to use larger width and heights than described above.
          This is because small mipmap levels may actually be stored within a larger block of memory, with an opaque amount of offseting which can interfere with alignment to cache lines.
        




## -see-also




<a href="https://msdn.microsoft.com/0AA10851-0077-4075-BD41-72FCD7BC0556">ID3D11Device3</a>
 

 

