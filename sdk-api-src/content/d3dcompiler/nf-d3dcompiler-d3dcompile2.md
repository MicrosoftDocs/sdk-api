---
UID: NF:d3dcompiler.D3DCompile2
title: D3DCompile2 function (d3dcompiler.h)
description: Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.
helpviewer_keywords: ["D3DCompile2","D3DCompile2 function [HLSL]","d3dcompiler/D3DCompile2","direct3dhlsl.d3dcompile2"]
old-location: direct3dhlsl\d3dcompile2.htm
tech.root: direct3dhlsl
ms.assetid: 0CE217EA-44F4-4017-B2ED-95E8B122CA95
ms.date: 12/05/2018
ms.keywords: D3DCompile2, D3DCompile2 function [HLSL], d3dcompiler/D3DCompile2, direct3dhlsl.d3dcompile2
req.header: d3dcompiler.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DCompile2
 - d3dcompiler/D3DCompile2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DCompile2
---

## -description

Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.

## -parameters

### -param pSrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to uncompiled shader data (ASCII HLSL code).

### -param SrcDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The size, in bytes, of the block of memory that <i>pSrcData</i> points to.

### -param pSourceName [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

An optional pointer to a constant null-terminated string containing the name that identifies the source data to use in error messages. If not used, set to <b>NULL</b>.

### -param pDefines [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D_SHADER_MACRO</a>*</b>

An optional array of <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D_SHADER_MACRO</a> structures that define shader macros. Each macro definition contains a name and a null-terminated definition. If not used, set to <b>NULL</b>. The last structure in the array serves as a terminator and must have all members set to <b>NULL</b>.

### -param pInclude [in, optional]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3dinclude">ID3DInclude</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3dinclude">ID3DInclude</a> interface that the compiler uses to handle include files. If you set this parameter to <b>NULL</b> and the shader contains a #include, a compile error occurs. You can pass the <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b> macro, which is a pointer to a default include handler. This default include handler includes files that are relative to the current directory and files that are relative to the directory of the initial source file. When you use <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b>, you must specify the source file name in the <i>pSourceName</i> parameter; the compiler will derive the initial relative directory from <i>pSourceName</i>.

```
#define D3D_COMPILE_STANDARD_FILE_INCLUDE ((ID3DInclude*)(UINT_PTR)1)
```

### -param pEntrypoint [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A pointer to a constant null-terminated string that contains  the name of the shader entry point function where shader execution begins. When you compile an effect, <b>D3DCompile2</b> ignores <i>pEntrypoint</i>; we recommend that you set <i>pEntrypoint</i> to <b>NULL</b> because it is good programming practice to set a pointer parameter to <b>NULL</b> if the called function will not use it.

### -param pTarget [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A pointer to a constant null-terminated string that specifies the shader target or set of shader features to compile against. The shader target can be a shader model (for example, shader model 2, shader model 3, shader model 4, or shader model 5). The target can also be an effect type (for example, fx_4_1). For info about the targets that various profiles support, see <a href="/windows/desktop/direct3dhlsl/specifying-compiler-targets">Specifying Compiler Targets</a>.

### -param Flags1 [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of shader <a href="/windows/desktop/direct3dhlsl/d3dcompile-constants">D3D compile constants</a> that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how the compiler compiles the HLSL code.

### -param Flags2 [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of effect <a href="/windows/desktop/direct3dhlsl/d3dcompile-effect-constants">D3D compile effect constants</a> that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how the compiler compiles the effect. When you compile a shader and not an effect file, <b>D3DCompile2</b> ignores <i>Flags2</i>; we recommend that you set <i>Flags2</i> to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.

### -param SecondaryDataFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of the following flags that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how the compiler compiles the HLSL code. 

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3DCOMPILE_SECDATA_MERGE_UAV_SLOTS (0x01)</td>
<td>Merge unordered access view (UAV) slots in the secondary data that the <i>pSecondaryData</i> parameter points to.</td>
</tr>
<tr>
<td>D3DCOMPILE_SECDATA_PRESERVE_TEMPLATE_SLOTS (0x02)</td>
<td>Preserve template slots in the secondary data that the <i>pSecondaryData</i> parameter points to.</td>
</tr>
<tr>
<td>D3DCOMPILE_SECDATA_REQUIRE_TEMPLATE_MATCH (0x04)</td>
<td>Require that templates in the secondary data that the <i>pSecondaryData</i> parameter points to match when the compiler compiles the HLSL code.</td>
</tr>
</table>

If <i>pSecondaryData</i> is <b>NULL</b>, set to zero.

### -param pSecondaryData [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to secondary data. If you don't pass secondary data, set to <b>NULL</b>. Use this secondary data  to align UAV slots in two shaders. Suppose shader A has UAVs and they are bound to some slots. To compile shader B such that UAVs with the same names are mapped in B to the same slots as in A, pass A’s byte code to <b>D3DCompile2</b> as the secondary data.

### -param SecondaryDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The size, in bytes, of the block of memory that <i>pSecondaryData</i> points to. If <i>pSecondaryData</i> is <b>NULL</b>, set to zero.

### -param ppCode [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the compiled code.

### -param ppErrorMsgs [out, optional]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access compiler error messages, or <b>NULL</b> if there are no errors.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

The difference between <b>D3DCompile2</b> and <a href="/windows/desktop/direct3dhlsl/d3dcompile">D3DCompile</a> is that <b>D3DCompile2</b> takes some optional parameters (<i>SecondaryDataFlags</i>, <i>pSecondaryData</i> and <i>SecondaryDataSize</i>)  that can be used to control some aspects of how bytecode is generated. Refer to the descriptions of these parameters for more details. There is no difference otherwise to the efficiency of the bytecode generated between  <b>D3DCompile2</b> and <b>D3DCompile</b>.

### Compiling shaders for UWP

To compile offline shaders the recommended approach is to use the <a href="/windows/desktop/direct3dtools/fxc">Effect-compiler tool</a>. If you can't compile all of your shaders ahead of time, then consider compiling the more expensive ones and the ones that your startup and most performance-sensitive paths require, and compiling the rest at runtime. You can use a process similar to the following to compile a loaded or generated shader in a UWP application without blocking your user interface thread.

* Using Visual Studio 2015+ to develop the UWP app, add the new item "shader.hlsl".
   * In the <b>Solution Folder</b> view of Visual Studio, select the <b>shaders.hlsl </b> item, right-click for <b>Properties</b>.
   * Make sure the item <b>Content</b> is set to <b>Yes</b>.
   * Make sure the <b>Item Type</b> is set to <b>Text</b>.
   * Add a button to XAML, name it appropriately ("TheButton" in this example), and add a <b>Click</b> handler.
* Now add these includes to your .cpp file:

   ``` syntax
   #include &lt;ppltasks.h&gt;
   #include &lt;d3dcompiler.h&gt;
   #include &lt;Robuffer.h&gt;
   ```

* Use the following code to call <b>D3DCompile2</b>. Note that there's no error checking or handling here, and also that this code demonstrates that you can do both I/O and compilation in the background, which leaves your UI more responsive.

```cppcx
void App1::DirectXPage::TheButton_Click(Platform::Object^ sender, Windows::UI::Xaml::RoutedEventArgs^ e)
{
  std::shared_ptr&lt;Microsoft::WRL::ComPtr&lt;ID3DBlob&gt;&gt; blobRef = std::make_shared&lt;Microsoft::WRL::ComPtr&lt;ID3DBlob&gt;&gt;();

  // Load a file and compile it.
  auto fileOp = Windows::ApplicationModel::Package::Current-&gt;InstalledLocation-&gt;GetFileAsync(L"shader.hlsl");
  create_task(fileOp).then([this](Windows::Storage::StorageFile^ file) -&gt; IAsyncOperation&lt;Windows::Storage::Streams::IBuffer^&gt;^
  {
    // Do file I/O in background thread (use_arbitrary).
    return Windows::Storage::FileIO::ReadBufferAsync(file);
  }, task_continuation_context::use_arbitrary())
    .then([this, blobRef](Windows::Storage::Streams::IBuffer^ buffer)
  {
    // Do compilation in background thread (use_arbitrary).

    // Cast to Object^, then to its underlying IInspectable interface.
    Microsoft::WRL::ComPtr&lt;IInspectable&gt; insp(reinterpret_cast&lt;IInspectable*&gt;(buffer));

    // Query the IBufferByteAccess interface.
    Microsoft::WRL::ComPtr&lt;Windows::Storage::Streams::IBufferByteAccess&gt; bufferByteAccess;
    insp.As(&amp;bufferByteAccess);

    // Retrieve the buffer data.
    byte *pBytes = nullptr;
    bufferByteAccess-&gt;Buffer(&amp;pBytes);

    Microsoft::WRL::ComPtr&lt;ID3DBlob&gt; blob;
    Microsoft::WRL::ComPtr&lt;ID3DBlob&gt; errMsgs;
    D3DCompile2(pBytes, buffer-&gt;Length, "shader.hlsl", nullptr, nullptr, "main", "ps_5_0", 0, 0, 0, nullptr, 0, blob.GetAddressOf(), errMsgs.GetAddressOf());
    *blobRef = blob;
  }, task_continuation_context::use_arbitrary())
    .then([this, blobRef]()
  {
    // Update UI / use shader on foreground thread.
    wchar_t message[40];
    swprintf_s(message, L"blob is %u bytes long", (unsigned)(*blobRef)-&gt;GetBufferSize());
    this-&gt;TheButton-&gt;Content = ref new Platform::String(message);
  }, task_continuation_context::use_current());
}
```

## -see-also

* <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>
* <a href="/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl">Specifying D3D12 Root Signatures in HLSL</a>
