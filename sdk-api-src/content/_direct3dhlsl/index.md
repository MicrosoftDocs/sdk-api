---
UID: TP:direct3dhlsl
ms.assetid: 351c8dd2-97c5-39de-8ade-c55ddf3acc2c
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# HLSL



Overview of the HLSL technology.

To develop HLSL, you need these headers:

 * [d3dcompiler.h](..\d3dcompiler\index.md)

For the programming guide, see [HLSL](https://review.docs.microsoft.com/en-us/win32-test/direct3dhlsl).

## Functions

| Title   | Description   |
| ---- |:---- |
| [D3DCompile function](..\d3dcompiler\nf-d3dcompiler-d3dcompile.md) | Compile HLSL code or an effect file into bytecode for a given target. |
| [D3DCompile2 function](..\d3dcompiler\nf-d3dcompiler-d3dcompile2.md) | Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target. |
| [D3DCompileFromFile function](..\d3dcompiler\nf-d3dcompiler-d3dcompilefromfile.md) | Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target. |
| [D3DCompressShaders function](..\d3dcompiler\nf-d3dcompiler-d3dcompressshaders.md) | Compresses a set of shaders into a more compact form. |
| [D3DCreateBlob function](..\d3dcompiler\nf-d3dcompiler-d3dcreateblob.md) | Creates a buffer. |
| [D3DCreateFunctionLinkingGraph function](..\d3dcompiler\nf-d3dcompiler-d3dcreatefunctionlinkinggraph.md) | Creates a function-linking-graph interface. |
| [D3DCreateLinker function](..\d3dcompiler\nf-d3dcompiler-d3dcreatelinker.md) | Creates a linker interface. Note  This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.  . |
| [D3DDecompressShaders function](..\d3dcompiler\nf-d3dcompiler-d3ddecompressshaders.md) | Decompresses one or more shaders from a compressed set. |
| [D3DDisassemble function](..\d3dcompiler\nf-d3dcompiler-d3ddisassemble.md) | Disassembles compiled HLSL code. |
| [D3DDisassemble10Effect function](..\d3dcompiler\nf-d3dcompiler-d3ddisassemble10effect.md) | Disassembles compiled HLSL code from a Direct3D10 effect. |
| [D3DDisassembleRegion function](..\d3dcompiler\nf-d3dcompiler-d3ddisassembleregion.md) | Disassembles a specific region of compiled Microsoft High Level Shader Language (HLSL) code. |
| [D3DGetBlobPart function](..\d3dcompiler\nf-d3dcompiler-d3dgetblobpart.md) | Retrieves a specific part from a compilation result. |
| [D3DGetDebugInfo function](..\d3dcompiler\nf-d3dcompiler-d3dgetdebuginfo.md) | Note  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store. Gets shader debug information. |
| [D3DGetInputAndOutputSignatureBlob function](..\d3dcompiler\nf-d3dcompiler-d3dgetinputandoutputsignatureblob.md) | Note  D3DGetInputAndOutputSignatureBlob may be altered or unavailable for releases after Windows 8.1. Instead use D3DGetBlobPart with the D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB value.  Gets the input and output signatures from a compilation result. |
| [D3DGetInputSignatureBlob function](..\d3dcompiler\nf-d3dcompiler-d3dgetinputsignatureblob.md) | Note  D3DGetInputSignatureBlob may be altered or unavailable for releases after Windows 8.1. Instead use D3DGetBlobPart with the D3D_BLOB_INPUT_SIGNATURE_BLOB value.  Gets the input signature from a compilation result. |
| [D3DGetOutputSignatureBlob function](..\d3dcompiler\nf-d3dcompiler-d3dgetoutputsignatureblob.md) | Note  D3DGetOutputSignatureBlob may be altered or unavailable for releases after Windows 8.1. Instead use D3DGetBlobPart with the D3D_BLOB_OUTPUT_SIGNATURE_BLOB value.  Gets the output signature from a compilation result. |
| [D3DGetTraceInstructionOffsets function](..\d3dcompiler\nf-d3dcompiler-d3dgettraceinstructionoffsets.md) | Retrieves the byte offsets for instructions within a section of shader code. |
| [D3DLoadModule function](..\d3dcompiler\nf-d3dcompiler-d3dloadmodule.md) | Creates a shader module interface from source data for the shader module. |
| [D3DPreprocess function](..\d3dcompiler\nf-d3dcompiler-d3dpreprocess.md) | Preprocesses uncompiled HLSL code. |
| [D3DReadFileToBlob function](..\d3dcompiler\nf-d3dcompiler-d3dreadfiletoblob.md) | Reads a file that is on disk into memory. |
| [D3DReflect function](..\d3dcompiler\nf-d3dcompiler-d3dreflect.md) | Gets a pointer to a reflection interface. |
| [D3DReflectLibrary function](..\d3dcompiler\nf-d3dcompiler-d3dreflectlibrary.md) | Creates a library-reflection interface from source data that contains an HLSL library of functions. |
| [D3DSetBlobPart function](..\d3dcompiler\nf-d3dcompiler-d3dsetblobpart.md) | Sets information in a compilation result. |
| [D3DStripShader function](..\d3dcompiler\nf-d3dcompiler-d3dstripshader.md) | Removes unwanted blobs from a compilation result. |
| [D3DWriteBlobToFile function](..\d3dcompiler\nf-d3dcompiler-d3dwriteblobtofile.md) | Writes a memory blob to a file on disk. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_D3D_SHADER_DATA structure](..\d3dcompiler\ns-d3dcompiler-_d3d_shader_data.md) | Describes shader data. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [D3DCOMPILER_STRIP_FLAGS enumeration](..\d3dcompiler\ne-d3dcompiler-d3dcompiler_strip_flags.md) | Strip flag options. |
| [D3D_BLOB_PART enumeration](..\d3dcompiler\ne-d3dcompiler-d3d_blob_part.md) | Values that identify parts of the content of an arbitrary length data buffer. |
